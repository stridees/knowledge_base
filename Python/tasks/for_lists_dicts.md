Переменной `books` присвоен список, элементами которого являются словари, содержащие информацию о книгах про Гарри Поттера

<details>
  <summary>Код</summary>
     
  ```python
 books = [
    {
        "title": "Harry Potter and the Philosopher's Stone",
        "author": "J.K. Rowling",
        "publication_year": 1997,
        "pages": 223,
        "language": "English",
        "publisher": "Bloomsbury",
        "price": 10.99,
        "weight": 0.45,
        "age_rating": "all ages",
        "main_characters": ["Harry Potter", "Ron Weasley", "Hermione Granger", "Albus Dumbledore", "Severus Snape"]
    },
    {
        "title": "Harry Potter and the Chamber of Secrets",
        "author": "J.K. Rowling",
        "publication_year": 1998,
        "pages": 251,
        "language": "English",
        "publisher": "Bloomsbury",
        "price": 11.99,
        "weight": 0.52,
        "age_rating": "all ages",
        "main_characters": ["Harry Potter", "Ron Weasley", "Hermione Granger", "Albus Dumbledore", "Rubeus Hagrid"]
    },
    {
        "title": "Harry Potter and the Prisoner of Azkaban",
        "author": "J.K. Rowling",
        "publication_year": 1999,
        "pages": 317,
        "language": "English",
        "publisher": "Bloomsbury",
        "price": 12.99,
        "weight": 0.61,
        "age_rating": "all ages",
        "main_characters": ["Harry Potter", "Ron Weasley", "Hermione Granger", "Albus Dumbledore", "Sirius Black"]
    },
    {
        "title": "Harry Potter and the Goblet of Fire",
        "author": "J.K. Rowling",
        "publication_year": 2000,
        "pages": 636,
        "language": "English",
        "publisher": "Bloomsbury",
        "price": 15.99,
        "weight": 0.91,
        "age_rating": "all ages",
        "main_characters": ["Harry Potter", "Ron Weasley", "Hermione Granger", "Albus Dumbledore", "Cedric Diggory"]
    },
    {
        "title": "Harry Potter and the Order of Phoenix",
        "author": "J.K. Rowling",
        "publication_year": 2003,
        "pages": 766,
        "language": "English",
        "publisher": "Bloomsbury",
        "price": 18.99,
        "weight": 1.03,
        "age_rating": "12+",
        "main_characters": ["Harry Potter", "Ron Weasley", "Hermione Granger", "Albus Dumbledore", "Luna Lovegood"]
    },
    {
        "title": "Harry Potter and the Half-Blood Prince",
        "author": "J.K. Rowling",
        "publication_year": 2005,
        "pages": 607,
        "language": "English",
        "publisher": "Bloomsbury",
        "price": 20.99,
        "weight": 0.95,
        "age_rating": "12+",
        "main_characters": ["Harry Potter", "Ron Weasley", "Hermione Granger", "Albus Dumbledore", "Draco Malfoy", "Horace Slughorn"]
    },
    {
        "title": "Harry Potter and the Deathly Hallows",
        "author": "J.K. Rowling",
        "publication_year": 2007,
        "pages": 759,
        "language": "English",
        "publisher": "Bloomsbury",
        "price": 22.99,
        "weight": 1.18,
        "age_rating": "12+",
        "main_characters": ["Harry Potter", "Ron Weasley", "Hermione Granger", "Albus Dumbledore", "Neville Longbottom", "Ginny Weasley"]
    }
 ]
``` 
</details>

Используя данные из указанного списка, необходимо выполнить следующие задания:

1. Распечатать все названия книг о Гарри Поттере, пронумеровав их
2. Вычислить и вывести на экран суммарное количество страниц во всех книгах
3. Вычислить и вывести на экран среднюю стоимость книги
4. Вывести названия книг с маркировкой "12+"
5. Вывести имена персонажей, которые содержатся во всех указанных выше словарях, но без повторений. Порядок вывода не имеет значения
6. Увеличить стоимость каждой книги в два раза, вывести данные о каждой книге в формате "Название - цена"
