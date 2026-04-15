Для выполнения лабораторной был склонирован репозиторий https://github.com/ververica/flink-training-exercises. 
В файле `utils/ExerciseBase.java` были изменены статические переменные `pathToRideData` и `pathToFareData`. 
Для удобства файлы `nycTaxiRides.gz` и `nycTaxiFares.gz` были размещены в корневой директории проекта, что позволило использовать относительные пути: data/nycTaxiRides.gz и data/nycTaxiFares.gz. 
Это гарантирует переносимость кода между различными средами.

<img width="880" height="124" alt="image" src="https://github.com/user-attachments/assets/67a50a52-60c2-4242-a9cc-807d4132eb47" />


Выполнены упражнения RideCleansingExercise, RidesAndFaresExercise, HourlyTipsExercise, ExpiringStateExercise. Все тесты успешно пройдены

* RideCleanisingTest: фильтрует поездки такси, оставляя только те, что начались и закончились в Нью-Йорке
<img width="416" height="182" alt="" src="https://github.com/user-attachments/assets/54aab128-f93a-481a-8f29-825d65b9cb02" />

* RidesAndFaresTest: объединяет (join) поток поездок и поток стоимости по rideId с использованием управляемого состояния
<img width="416" height="190" alt="" src="https://github.com/user-attachments/assets/56be1674-cc78-4819-b391-81640ba706c8" />

* HourlyTipsTest: вычисляет максимальную сумму чаевых, полученных одним водителем за каждый час
<img width="424" height="199" alt="" src="https://github.com/user-attachments/assets/5091d732-f45b-46a2-9fa0-faf8bf9cb03b" />

* ExpiringStateTest: расширяет RidesAndFares, добавляя таймеры для очистки "висящих" в состоянии данных и отправляет их в Side Output
<img width="429" height="182" alt="" src="https://github.com/user-attachments/assets/435e5cd1-cf0c-4eff-8118-d6782d858eee" />
