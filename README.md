# Втора лабораториска вежба по Софтверско инженерство

## Љубомир Давитков 216092
### Control Flow Graph
![](C:\Users\User\Downloads\silab2SLIKA.png)
### Цикломатска комплексност
Цикломатската комплексност на овој код е 9, истата ја добив преку формулата P+1, каде што P е бројот на предикатни јазли. Во случајoв P=1, па цикломатската комплексност изнесува 9.

### Тест случаи според критериумот Every Branch
1. Тест случај кога user e null
 - Влез: user = null, allUsers = [user1, user2, ...]
 - Очекуван излез: RuntimeException("Mandatory information missing!")
2. Тест случај кога user.getPassword() е null
 - Влез: user = new User("username", null, "email"), allUsers = [user1, user2, ...]
 - Очекуван излез: RuntimeException("Mandatory information missing!")
3. Тест случај кога user.getEmail() е null
 - Влез: user = new User("username", "password", null), allUsers = [user1, user2, ...]
 - Очекуван излез: RuntimeExeption("Mandatory information missing!")
4. Тест случај кога user.getUsername() е null и user.getEmail() не е null
 - Влез: user = new User(null, "password", "email"), allUsers = [user1, user2, ...]
 - Очекуван излез: user.getUsername() треба да е сетиран на user.getEmail()
5. Тест случај кога user.getEmail() не содржи '@' or '.':
 - Влез: user = new User("username", "password", "invalidemail"), allUsers = [user1, user2, ...]
 - Очекуван излез: same треба да е еднакво на 1
6. Тест случај кога user.getEmail() содржи '@' or '.':
 - Влез: user = new User("username", "password", "valid@email"), allUsers = [user1, user2, ...]
 - Очекуван излез: same треба да е еднакво на бројот на корисници со исти email и username
7. Тест случај кога passwordLower содржи user.getUsername().toLowerCase()
 - Влез: user = new User("username", "password", "email"), allUsers = [user1, user2, ...]
 - Очекуван излез: false
8. Тест случај кога password.length() е помалку од 8
 - Влез: user = new User("username", "pass", "email"), allUsers = [user1, user2, ...]
 - Излез: false
9. Тест случај кога passwordLower не содржи ниту едно празно место или специјален карактер
 - Влез: user = new User("username", "password", "email"), allUsers = [user1, user2, ...]
 - Очекуван излез: false
10. Тест случај кога same е 0
 - Влез: user = new User("username", "password", "email"), allUsers = []
 - Очекуван излез: true


### Тест случаи според критериумот Multiple Condition
1. Тест случај кога user e null
 - Влез: user = null
 - Очекуван излез: RuntimeException("Mandatory information missing!")
2. Тест случај кога user.getPassword() е null
 - Влез: user = new User("username", null, "email")
 - Очекуван излез: RuntimeException("Mandatory information missing!")
3. Тест случај кога user.getEmail() е null
 - Влез: user = new User("username", "password", null)
 - Очекуван излез: RuntimeException("Mandatory information missing!")
4. Тест случај каде што се исполнети сите услови
 - Влез: user = new User("username", "password", "email")
 - Очекуван излез: No exception is thrown