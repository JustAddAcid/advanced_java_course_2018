# В камках курса "Углубленное изучение JAVA -- Технополис Mail.ru"

Реализованная специальным образом строка (аналог java.lang.String),
хранящий содержимое строки кусочкам (chunks) для лучшего переиспользования памяти при активном
создании подстрок.    

Представляет собой класс для хранение строк большой длины        
Минимальная структурная единица в таком случае не символ, а чанк    
При инициализации строка разбивается на чанки заданной длины (если не указано -- длиной 1/100 от общей)    
     
При выделении подстроки формируется массив ссылок на старые чанки, которые вошли в подстроку    
        -> не дублируются данные

При сериализации объекта, данные из родительской строки, которые НЕ вошли в дочернюю    
        -> не участвуют в сериализации

Проверка с большим текстом в main()    
