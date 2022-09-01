
# Requisitos
Antes de ocupar el módulo, asegúrate de tener los siguientes requisitos.

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

> **NOTA:** La *baseURL* depende del ambiente que se desee ocupar (uat, pre-prod, prod) y de la licencia proporcionada, **no todas las licencias estás dadas de altas en todos los ambientes**.

## 2) Credenciales de Producto

Solicitar al equipo de **producto** un usaurio de Na-at Technologies relacionada con el cliente, producto devolverá son los siguientes datos:

> **Usuario**:\
ejemplo.empresa.proyecto@na-at-com.mx\
**Contraseña:**\
xxxxxxxxxxxxxxxxxxxxxxxxxxxxx


Una vez creada la cuenta deben acceder a la siguiente url para generar su token:

https://devapiframe.firmaautografa.com/token-generator

<div>
<img src="https://raw.githubusercontent.com/lgeronimov/resoruces/master/images/token-generator.png" width="500"/>
</div>

Este es el token que se requiere para poder inicializar el iframe:

``` ts
.
.
const tkn = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
const url = `https://devapiframe.firmaautografa.com/fad-iframe-facetec?tkn=${tkn}`;
.
.
```

Una vez obtenido todo esto, ya podrás hacer uso del módulo.