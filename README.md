## :construction: - Eventos Tec
- Backend for eventos tec
- Aplicação para gerenciar eventos de tecnologia, permitindo o:
  -  cadastro;
  -  listagem;
  -  filtragem;
  -  detalhamento de eventos;
  -  associação de cupons de desconto.

##

## 📋 - Diagrama de Classes:

```mermaid
classDiagram
  class Event {
    -UUID id
    -String title
    -String description
    -String imgUrl
    -String eventUrl
    -Boolean remote
    -Date date
  }

  class Address {
    -UUID id
    -String city
    -String uf
    -Event event
  }

  class Publisher {
    -UUID id
    -String code
    -Integer discount
    -Date valid
    -Event event
  }

  Event "N" *-- "N" Address
  Event "1" *-- "N" Publisher
```

##

## ⚙️ - Diagrama de Funcionalidade:

![eventos drawio](https://github.com/carloshenriquefs/eventos-tec/assets/54969405/6fb27927-97ff-4d99-9ac5-5c5c449c0e01)
