# ionic
## Instalação Node/NPM

https://nodejs.org/en/download/

npm install

npm install -g ionic cordova

#### node -v
#### npm -v
#### cordova -v

https://ionicframework.com/getting-started#cli

#### $ ionic start myApp sidemenu

#### $ ionic serve

## Excluir Página
1. Apagar Pasta

2. Apagar as referências e app.module.ts e app.component.ts

# Lazy Loading (sidemenu)
### Criar o arquivo home.module.ts na pagina home

import { IonicPageModule } from 'ionic-angular/module';
import { NgModule } from '@angular/core';
import { HomePage } from './home';
@NgModule({
 declarations: [HomePage],
 imports: [IonicPageModule.forChild(HomePage)]
})
export class HomeModule {
}

### Em home.ts, incluir @IonicPage()
import { Component } from '@angular/core';
import { NavController, IonicPage } from 'ionic-angular';

@IonicPage()
@Component({
  selector: 'page-home',
  templateUrl: 'home.html'
})
export class HomePage {
  constructor(public navCtrl: NavController) {
  }
}

