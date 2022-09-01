
# Requisitos
Antes de ocupar el módulo, asegúrate de tener cumplir con los siguientes requisitos

## 1) Licencia de Facetec

Solicita al equipo de **tecnología** de Na-at Technologies una licencia de facetec asociada a tu proyecto. 

``` ts
  deviceKeyIdentifier: 'XXXXXXXXXXXXXXXXXX',
  baseURL: '',
  publicFaceScanEncryptionKey: '-----BEGIN PUBLIC KEY-----\n' +
    'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX' +
    'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX' +
    'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX' +
    'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX' +
    '-----END PUBLIC KEY-----',
  productionKeyText: {
    domains: 'XXXXXXXXXXXXXXXXXX',
    expiryDate: 'XXXX-XX-XX',
    key: 'XXXXXXXXXXXXXXXXXX'
  }
```

Esta licencia es la que ocuparás el apartado de *CREDENTIALS* del ejemplo.

> **NOTA:** La *baseURL* depende del ambiente que se desee ocupar (uat, prod, etc.)

## 2) Credenciales de Producto

Solicitar al equipo de **producto** un usaurio de Na-at Technologies relacionada con el cliente, producto devolverá son los siguientes datos:

> **Usuario**:\
ejemplo.empresa.proyecto@na-at-com.mx\
**Contraseña:**\
xxxxxxxxxxxxxxxxxxxxxxxxxxxxx


Una vez creada la cuenta deden acceder a la siguiente url para generar su token:

https://devapiframe.firmaautografa.com/token-generator

<div>
<img src="https://raw.githubusercontent.com/lgeronimov/resoruces/master/images/token-generator.png" width="500"/>
</div>

Este es el token que se requiere para poder iniciarlizar el iframe:

``` ts
.
.
const tkn = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
const url = `https://devapiframe.firmaautografa.com/fad-iframe-facetec?tkn=${tkn}`;
.
.
```

Una vez obtenido todo esto, ya podrás hacer uso del módulo.