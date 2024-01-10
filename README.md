# CRIAR E PUBLICAR UM APP REACT NATIVE + EXPO

```
# Criando um projeto
npx create-expo-app app
cd app
```

```
# Instalar dependencia para executar o projeto no navegador web
npm i react-native-web@~0.19.6
npm i react-dom@18.2.0
npm i @expo/webpack-config@^19.0.0 
```


```
# Site para praticar flexbox
https://flexboxfroggy.com/
```

```
# Executar o projeto em sua máquina
npm run android
npm run ios
npm run web
```


------------------------------------------------
####EAS - Enterprise Application Services
- EAS é Enterprise Application Services - É um serviço do Expo para publicar seu aplicativo em ambiente de desenvolvimento, homologação e produção.
- OBS: Antes de usar o EAS, é preciso abrir uma conta no expo.dev.

```
# INSTALANDO EAS PARA buildar nosso projeto:
npm i -g eas-cli
```

```
# Vinculando seu PC a sua conta Expo. Execute os comandos abaixo:
eas login

- Informe seu email e senha. A mesma informada no Expo.

```

```
# Cadastrando seu projeto no expo. Execute:
eas init
```


```
# Subindo atualizações do seu projeto no expo.dev
eas update --branch preview --message "O que voce fez?"
```

```
# Build do projeto para publicação na Play Store e App Store
eas build --platform android
eas build --platform ios
```

```
# Gerando uma APK para seu(ua) amigo(a)!
# OBS: Antes de executar o comando abaixo, deve ser configurado o arquivo de eas.json com as informações abaixo:

eas build --platform android --profile preview



# Configurações do eas.json


{
  "build": {
    "preview": {
      "android": {
        "buildType": "apk"
      }
    },
    "preview2": {
      "android": {
        "gradleCommand": ":app:assembleRelease"
      }
    },
    "preview3": {
      "developmentClient": true
    },
    "preview4": {
      "distribution": "internal"
    },
    "production": {}
  }
}

```
