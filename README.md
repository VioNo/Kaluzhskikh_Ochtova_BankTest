# Автоматизирование тестирование проекта BankAccount
## Тестирование метода Debit
1. Тест `Debit_WithValidAmount_UpdatesBalance`:
![изображение](https://github.com/user-attachments/assets/92e06d9b-0cca-4e01-a35c-ad481a66905a)
Тест не прошел. Это связано с логической ошибкой в методе `Debit`, который увеличивал баланс вместо уменьшения. После исправления этой ошибки (замена `m_balance += amount;` на `m_balance -= amount;`) тест успешно проходит, что подтверждает корректность операции списания средств.
![изображение](https://github.com/user-attachments/assets/508cf462-e4de-426c-add6-42bb455e4eb9)

2. Тест `Debit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange`:
![изображение](https://github.com/user-attachments/assets/de2f8b91-7a1f-4e82-8f38-737c679f511f)
Тест успешно пройден. Это означает, что метод `Debit` корректно выбрасывает исключение ArgumentOutOfRangeException при попытке списать отрицательную сумму. Успешное выполнение теста подтверждает правильность обработки данного условия.

3. Тест `Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange`:
![изображение](https://github.com/user-attachments/assets/87377d62-1434-4ce1-b89b-69e9f1e26c9c)
Тест успешно пройден. Это означает, что метод `Debit` корректно выбрасывает исключение ArgumentOutOfRangeException при попытке списать сумму, превышающую текущий баланс. Успешное выполнение теста подтверждает правильность обработки данного условия.

***
## Тестирование метода Credit
![изображение](https://github.com/user-attachments/assets/4024d91f-40d7-4bbc-ad7b-7dd7f6a23460)
1. 
