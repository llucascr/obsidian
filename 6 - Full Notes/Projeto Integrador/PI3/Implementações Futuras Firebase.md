
2025-03-31

Status:

Tags: [[Projeto Integrador 3]]

---

# Funcionalidade

Vamos usar isso para guardar códigos padrão do Firebase para futuramente melhorar a eficiência de implementarmos as funcionalidades.

## Firebase Firestore

## Método de criação de um documento para salvar no Firestore

```kotlin
fun addNewTestTask() {  
    // Referencia do singleton firestore  
    val db = Firebase.firestore  
  
    val taskTestDoc = hashMapOf(  
        "nome" to "Nome da tarefa de testes...",  
        "descrição" to "Descrição teste..."  
    )  
  
    db.collection("tasks").add(taskTestDoc)  
}
```

## Firebase Auth

### Método de criação da conta autorizada

```kotlin
fun createTestAccount() {  
    val auth = Firebase.auth  
    auth.createUserWithEmailAndPassword(  
        "teste@teste.com.br", "1234567qwerty")  
        .addOnCompleteListener {task ->  
            if (task.isSuccessful) {  
                Log.i("AUTH-INFO",  
                    "Usuario criado com suscesso: ${task.result.user!!.uid}")  
            }else {  
                Log.e("AUTH-INFO", "ERRO ao criar o usuário: " +  
                        "${task.exception}")  
            }  
        }  
}
```



---
# Referências
