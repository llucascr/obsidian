
2025-03-28

Status:

Tags: [[Firebase]]

---

# Regras do Service Firestore:

```groovy
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if false;
    }
  }
}
```


## Mudar para: 

```groovy
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write;
    }
  }
}
```


> <font color="#ff0000">Suas regras de segurança estão definidas como públicas. Com essa configuração, qualquer pessoa pode roubar, modificar ou excluir informações do seu banco de dados</font>


---
# Referências
[[Firebase]]
