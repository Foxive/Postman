[![D|](https://lentux-informatica.com/wp-content/uploads/2018/05/postman-logo.png)](https://www.postman.com/)
## __Homeworks status:__ _finished_
---
-  [HW_1](#hw_1)
    - [collection_1][hw1col_link]
    - [testrun_1][hw1test_link]
- [HW_2](#hw_2)
    - [collection_2][hw2col_link]
    - [testrun_2][hw2test_link]
    - [env][hw2env_link]
- [HW_3](#hw_3)
    - [collection_3][hw3col_link]
    - [testrun_3][hw3test_link]
    - [env][hw3env_link]
--- 

## Learned skills

-   Proficiency in using Postman for API testing 
-   Ability to create and execute API tests using Postman 
-   Writing test scripts using JavaScript (Chai.js)
-   Automating test using collection runner
-   Debugging and troubleshooting errors in API requests/responses/tests
-   Understanding of HTTP requests and responses (e.g. CRUD methods/Status codes)
-   Working with different types of authentication methods such passwords, API keys, etc
-   Strong problem-solving skills for identifying and resolving issues
-   Strong communication skills for sharing test results and reporting issues

---

## HW 1 <a name="hw_1"></a>

<details>
<summary>Homework 1</summary>

*Main task: Создать запросы в Postman.*
```javascript
Protocol: http
IP: **
Port: 5005
```

```javascript
EP_1
Method: GET
EndPoint: /get_method
    request url params: 
    name: str
    age: int
        response: 
        [   “Str”,
            “Str”]
```

```javascript
EP_2
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
```

```javascript
EP_3
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int

response: 
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
```

```javascript
EP_4
Method: GET
EndPoint: /object_info_2
request url params: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```

```javascript
EP_5
Method: GET
EndPoint: /object_info_3
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }
```

```javascript
EP_6
Method: GET
EndPoint: /object_info_4
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}
```

```javascript
EP_7
Method: POST
EndPoint: /user_info_2
request form data: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```

</details>

---
## HW 2 <a name="hw_2"></a>

<details>
<summary>Homework 2</summary>

*Main tasks:* 
* Отправить запрос
* Проверить статус код (== 200)
* Проверить доп. параметры с помощью тестов

<details>
<summary>Tasks</summary>
<details>
<summary>Task 1 (EP_1)</summary>

```javascript
{{url}}/first
1. Отправить запрос.
2. Статус код 200
3. Проверить, что в body приходит правильный string.
```

</details>
<details>
<summary>Task 2 (EP_2)</summary>

```javascript
{{url}}/user_info_3
1. Отправить запрос.
2. Статус код 200
3. Спарсить response body в json.
4. Проверить, что name в ответе равно name s request (name вбить руками.)
5. Проверить, что age в ответе равно age s request (age вбить руками.)
6. Проверить, что salary в ответе равно salary s request (salary вбить руками.)
7. Спарсить request.
8. Проверить, что name в ответе равно name s request (name забрать из request.)
9. Проверить, что age в ответе равно age s request (age забрать из request.)
10. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
11. Вывести в консоль параметр family из response.
12. Проверить что u_salary_1_5_year в ответе равно salary*4 (salary забрать из request)
```

</details>
<details>
<summary>Task 3 (EP_3)</summary>

```javascript
{{url}}/object_info_3
1. Отправить запрос.
2. Статус код 200
3. Спарсить response body в json.
4. Спарсить request.
5. Проверить, что name в ответе равно name s request (name забрать из request.)
6. Проверить, что age в ответе равно age s request (age забрать из request.)
7. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
8. Вывести в консоль параметр family из response.
9. Проверить, что у параметра dog есть параметры name.
10. Проверить, что у параметра dog есть параметры age.
11. Проверить, что параметр name имеет значение Luky.
12. Проверить, что параметр age имеет значение 4.
```

</details>
<details>
<summary>Task 4 (EP_4)</summary>

```javascript
{{url}}/object_info_4
1. Отправить запрос.
2. Статус код 200
3. Спарсить response body в json.
4. Спарсить request.
5. Проверить, что name в ответе равно name s request (name забрать из request.)
6. Проверить, что age в ответе равно age из request (age забрать из request.)
7. Вывести в консоль параметр salary из request.
8. Вывести в консоль параметр salary из response.
9. Вывести в консоль 0-й элемент параметра salary из response.
10. Вывести в консоль 1-й элемент параметра salary параметр salary из response.
11. Вывести в консоль 2-й элемент параметра salary параметр salary из response.
12. Проверить, что 0-й элемент параметра salary равен salary из request (salary забрать из request.)
13. Проверить, что 1-й элемент параметра salary равен salary*2 из request (salary забрать из request.)
14. Проверить, что 2-й элемент параметра salary равен salary*3 из request (salary забрать из request.)
15. Создать в окружении переменную name
16. Создать в окружении переменную age
17. Создать в окружении переменную salary
18. Передать в окружение переменную name
19. Передать в окружение переменную age
20. Передать в окружение переменную salary
21. Написать цикл который выведет в консоль по порядку элементы списка из параметра salary.
```

</details>
<details>
<summary>Task 5 (EP_5)</summary>

```javascript
{{url}}/user_info_2
1. Вставить параметр salary из окружения в request
2. Вставить параметр age из окружения в age
3. Вставить параметр name из окружения в name
4. Отправить запрос.
5. Статус код 200
6. Спарсить response body в json.
7. Спарсить request.
8. Проверить, что json response имеет параметр start_qa_salary
9. Проверить, что json response имеет параметр qa_salary_after_6_months
10. Проверить, что json response имеет параметр qa_salary_after_12_months
11. Проверить, что json response имеет параметр qa_salary_after_1.5_year
12. Проверить, что json response имеет параметр qa_salary_after_3.5_years
13. Проверить, что json response имеет параметр person
14. Проверить, что параметр start_qa_salary равен salary из request (salary забрать из request.)
15. Проверить, что параметр qa_salary_after_6_months равен salary*2 из request (salary забрать из request.)
16. Проверить, что параметр qa_salary_after_12_months равен salary*2.7 из request (salary забрать из request.)
17. Проверить, что параметр qa_salary_after_1.5_year равен salary*3.3 из request (salary забрать из request.)
18. Проверить, что параметр qa_salary_after_3.5_years равен salary*3.8 из request (salary забрать из request.)
19. Проверить, что в параметре person, 1-й элемент из u_name равен salary из request (salary забрать из request.)
20. Проверить, что что параметр u_age равен age из request (age забрать из request.)
21. Проверить, что параметр u_salary_5_years равен salary*4.2 из request (salary забрать из request.)
22. ***Написать цикл который выведет в консоль по порядку элементы списка из параметра person.
```

</details>
</details>


<details>
<summary>Code</summary>
<details>
<summary>Task 1 (EP_1)</summary>

```javascript
// Парсим ответ
var testBody = pm.response.text();
// 2. Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 3. Проверить, что в body приходит правильный string.
pm.test("Body matches string", function () {
    pm.expect(pm.response.text()).to.include("This is the first responce from server!ss");
});
pm.test("Body is correct", function () {
    pm.response.to.have.body(testBody);
});
```

</details>
<details>
<summary>Task 2 (EP_2)</summary>

```javascript
// 2. Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 3. Спарсить response body в json.
const responseJson = pm.response.json();
// 4. Проверить, что name в ответе равно name s request (name вбить руками.)
pm.test("Person is John", () => {
  pm.expect(responseJson.name).to.eql("John");
});
// 5. Проверить, что age в ответе равно age s request (age вбить руками.)
pm.test("Age is 25", () => {
  pm.expect(responseJson.age).to.eql+(25);
});
// 6. Проверить, что salary в ответе равно salary s request (salary вбить руками.)
pm.test("Salary is 1000", () => {
  pm.expect(responseJson.salary).to.eql(1000);
});
// 7. Спарсить request.
var requestdata = request.data;
// 8. Проверить, что name в ответе равно name s request (name забрать из request.)
pm.test("Person name is valid", () => {
  pm.expect(responseJson.name).to.eql(requestdata.name);
});
// 9. Проверить, что age в ответе равно age s request (age забрать из request.)
pm.test("Person age is valid", () => {
  pm.expect(responseJson.age).to.eql(requestdata.age);
});
// 10. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
pm.test("Person salary is valid", () => {
  pm.expect(responseJson.salary).to.eql(+requestdata.salary);
});
// 11. Вывести в консоль параметр family из response.
console.log (responseJson.family)
// 12. Проверить что u_salary_1_5_year в ответе равно salary*4 (salary забрать из request)
pm.test("Server logic works out multiplication", () => {
  pm.expect(responseJson.family.u_salary_1_5_year).to.eql(requestdata.salary*4);
});
```
</details>
<details>
<summary>Task 3 (EP_3)</summary>

```javascript
// 2. Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 3. Спарсить response body в json.
const responseJson = pm.response.json();
// 4. Спарсить request
var requestdata = pm.request.url.query.toObject();
// 5. Проверить, что name в ответе равно name s request (name забрать из request.)
pm.test("Person name is valid", () => {
  pm.expect(responseJson.name).to.eql(requestdata.name);
});
// 6. Проверить, что age в ответе равно age s request (age забрать из request.)
pm.test("Person age is valid", () => {
  pm.expect(responseJson.age).to.eql(requestdata.age);
});
// 7. Проверить, что salary в ответе равно salary s request (salary забрать из request.)
pm.test("Person salary is valid", () => {
  pm.expect(responseJson.salary).to.eql(+requestdata.salary);
});
// 8. Вывести в консоль параметр family из response.
console.log (responseJson.family)
// 9. Проверить, что у параметра dog есть параметры name.
pm.test("Dog name is valid", () => {
  pm.expect(responseJson.family.pets.dog).to.have.property("name");
});
// 10. Проверить, что у параметра dog есть параметры age.
pm.test("Dog age is valid", () => {
  pm.expect(responseJson.family.pets.dog).to.have.property("age");
});
// 11. Проверить, что параметр name имеет значение Luky.
pm.test("Dog name is Luky", () => {
  pm.expect(responseJson.family.pets.dog.name).to.eql("Luky")
});
// 12. Проверить, что параметр age имеет значение 4.
pm.test("Dog age is 4", () => {
  pm.expect(responseJson.family.pets.dog.age).to.eql(4)
});
```
</details>
<details>
<summary>Task 4 (EP_4)</summary>

```javascript
// 2. Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 3. Спарсить response body в json.
const responseJson = pm.response.json();
// 4. Спарсить request
var requestdata = pm.request.url.query.toObject();
// 5. Проверить, что name в ответе равно name s request (name забрать из request.)
pm.test("Person name is valid", () => {
  pm.expect(responseJson.name).to.eql(requestdata.name);
});
// 6. Проверить, что age в ответе равно age s request (age забрать из request.)
pm.test("Person age is valid", () => {
  pm.expect(responseJson.age).to.eql(+requestdata.age);
});
// 7. Вывести в консоль параметр salary из request.
console.log(requestdata.salary)
// 8. Вывести в консоль параметр salary из response.
console.log(responseJson.salary)
// 9. Вывести в консоль 0-й элемент параметра salary из response.
console.log(responseJson.salary[0])
// 10. Вывести в консоль 1-й элемент параметра salary параметр salary из response.
console.log(responseJson.salary[1])
// 11. Вывести в консоль 2-й элемент параметра salary параметр salary из response.
console.log(responseJson.salary[2])
// 12. Проверить, что 0-й элемент параметра salary равен salary из request (salary забрать из request.)
pm.test("Server response equal request ", () => {
  pm.expect(responseJson.salary[0]).to.eql(+requestdata.salary);
});
// 13. Проверить, что 1-й элемент параметра salary равен salary*2 из request (salary забрать из request.)
pm.test("Server response equal request ", () => {
  pm.expect(+responseJson.salary[1]).to.eql(requestdata.salary*2);
});
// 14. Проверить, что 2-й элемент параметра salary равен salary*3 из request (salary забрать из request.)
pm.test("Server response equal request ", () => {
  pm.expect(+responseJson.salary[2]).to.eql(requestdata.salary*3);
});
// 15. Создать в окружении переменную name
pm.environment.set("name", " ");
// 16. Создать в окружении переменную age
pm.environment.set("age", " ");
// 17. Создать в окружении переменную salary
pm.environment.set("salary", " ");
// 18. Передать в окружение переменную name
pm.environment.set("name", requestdata.name);
// 19. Передать в окружение переменную age
pm.environment.set("age", requestdata.age);
// 20. Передать в окружение переменную salary
pm.environment.set("salary", requestdata.salary);
// // 21. Написать цикл который выведет в консоль по порядку элементы списка из параметра salary.
var arr = responseJson.salary
console.log ('asd')
arr.forEach(function(item, i, arr) {
    console.log ('Текущий элемент списка: ', i, ' имеет значение =', item)
})
```
</details>
<details>
<summary>Task 5 (EP_5)</summary>

```javascript
// 5. Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 6. Спарсить response body в json.
const responseJson = pm.response.json();
// // 7. Спарсить request
var requestdata = request.data
console.log(requestdata)
// // 8. Проверить, что json response имеет параметр start_qa_salary
pm.test("Json response have property start_qa_salary", () => {
  pm.expect(responseJson).to.have.property("start_qa_salary")
});
// 9. Проверить, что json response имеет параметр qa_salary_after_6_months
pm.test("Json response have property qa_salary_after_6_months", () => {
  pm.expect(responseJson).to.have.property("qa_salary_after_6_months")
});
// 10. Проверить, что json response имеет параметр qa_salary_after_12_months
pm.test("Json response have property qa_salary_after_12_months", () => {
  pm.expect(responseJson).to.have.property("qa_salary_after_12_months")
});
// 11. Проверить, что json response имеет параметр qa_salary_after_1.5_year
pm.test("Json response have property qa_salary_after_1.5_year", () => {
  pm.expect(responseJson).to.have.property("qa_salary_after_1.5_year")
});
// 12. Проверить, что json response имеет параметр qa_salary_after_3.5_years
pm.test("Json response have property qa_salary_after_3.5_years", () => {
  pm.expect(responseJson).to.have.property("qa_salary_after_3.5_years")
});
// 13. Проверить, что json response имеет параметр person
pm.test("Json response have property person", () => {
  pm.expect(responseJson).to.have.property("person")
});
// 14. Проверить, что параметр start_qa_salary равен salary из request (salary забрать из request.)
pm.test("Param response start_qa_salary eql salary from request", () => {
    pm.expect(responseJson.start_qa_salary).to.eql(+requestdata.salary);
});
// 15. Проверить, что параметр qa_salary_after_6_months равен salary*2 из request (salary забрать из request.)
pm.test("Param response qa_salary_after_6_months eql salary*2 from request", () => {
    pm.expect(responseJson.qa_salary_after_6_month).to.eql+(requestdata.salary*2);
});
// 16. Проверить, что параметр qa_salary_after_12_months равен salary*2.7 из request (salary забрать из request.)
pm.test("Param response qa_salary_after_12_months eql salary*2 from request", () => {
    pm.expect(responseJson.qa_salary_after_12_month).to.eql+(requestdata.salary*2.7);
});
// 17. Проверить, что параметр qa_salary_after_1.5_year равен salary*3.3 из request (salary забрать из request.)
pm.test("Param response qa_salary_after_1.5_years eql salary*2 from request", () => {
    pm.expect(responseJson["qa_salary_after_1.5_years"]).to.eql+(requestdata.salary*3.3);
});
// 18. Проверить, что параметр qa_salary_after_3.5_years равен salary*3.8 из request (salary забрать из request.)
pm.test("Param response qa_salary_after_3.5_years eql salary*2 from request", () => {
    pm.expect(responseJson["qa_salary_after_3.5_years"]).to.eql+(requestdata.salary*3.8);
});
// 19. Проверить, что в параметре person, 1-й элемент из u_name равен salary из request (salary забрать из request.)
pm.test("1st element in param person from u_name = salary", () => {
    pm.expect(responseJson.person.u_name[1]).to.eql+(requestdata.salary);
});
// 20. Проверить, что что параметр u_age равен age из request (age забрать из request.)
pm.test("Param age from u_name = age", () => {
    pm.expect(responseJson.person.u_name[2]).to.eql+(requestdata.age);
});
// 21. Проверить, что параметр u_salary_5_years равен salary*4.2 из request (salary забрать из request.)
pm.test("Param u_salary_5_years", () => {
    pm.expect(responseJson.person.u_salary_5_years).to.eql+(requestdata.salary*4.2);
});
// 22. ***Написать цикл который выведет в консоль по порядку элементы списка из параметра person.
for (i in responseJson.person) {
 console.log('Element: ', responseJson.person[i]);
}
```

</details>
</details>
</details>

---

## HW 3 <a name="hw_3"></a>
<details>
<summary>Homework 3</summary>


*Main tasks:* 
*  Отправить запрос
*  Получить токен
*  Проверить доп. параметры с помощью тестов


<details>
<summary>Tasks</summary>
<details>
<summary>Task 1 (EP_1)</summary>

```javascript
POST
{{url}}/login
login : str (кроме /)
password : str
Приходящий токен необходимо передать во все остальные запросы.
```

</details>
<details>
<summary>Task 2 (EP_2)</summary>

```javascript
{{url}}/user_info
    req. (RAW JSON)
    POST
    age: int
    salary: int
    name: str
    auth_token
    resp.
    {'start_qa_salary':salary,
    'qa_salary_after_6_months': salary * 2,
    'qa_salary_after_12_months': salary * 2.9,
    'person': {'u_name':[user_name, salary, age],
                                'u_age':age,
                                'u_salary_1.5_year': salary * 4}
                                }
Тесты:
1) Статус код 200
2) Проверка структуры json в ответе.
3) В ответе указаны коэффициенты умножения salary, напишите тесты по проверке правильности результата перемножения на коэффициент.
4) Достать значение из поля 'u_salary_1.5_year' и передать в поле salary запроса {{url}}/get_test_user

```
</details>
<details>
<summary>Task 3 (EP_3)</summary>

```javascript
{{url}}/new_data
    req.
    POST
    age: int
    salary: int
    name: str
    auth_token
    Resp.
    {'name':name,
    'age': int(age),
    'salary': [salary, str(salary*2), str(salary*3)]}
Тесты:
1) Статус код 200
2) Проверка структуры json в ответе.
3) В ответе указаны коэффициенты умножения salary, напишите тесты по проверке правильности результата перемножения на коэффициент.
4) проверить, что 2-й элемент массива salary больше 1-го и 0-го

```
</details>
<details>
<summary>Task 4 (EP_4)</summary>

```javascript
 {{url}}/test_pet_info    
    req.
    POST
    age: int
    weight: int
    name: str
    auth_token
    Resp.  
    {'name': name,
    'age': age,
    'daily_food':weight * 0.012,
    'daily_sleep': weight * 2.5}
Тесты:
1) Статус код 200
2) Проверка структуры json в ответе.
3) В ответе указаны коэффициенты умножения weight, напишите тесты по проверке правильности результата перемножения на коэффициент.
```
</details>
<details>
<summary>Task 5 (EP_5)</summary>

```javascript
{{url}}/get_test_user
    req.
    POST
    age: int
    salary: int
    name: str
    auth_token

    Resp.
    {'name': name,
    'age':age,
    'salary': salary,
    'family':{'children':[['Alex', 24],['Kate', 12]],
    'u_salary_1.5_year': salary * 4}
    }
Тесты:
1) Статус код 200
2) Проверка структуры json в ответе.
3) Проверить что занчение поля name = значению переменной name из окружения
4) Проверить что занчение поля age в ответе соответсвует отправленному в запросе значению поля age
```

</details>
<details>
<summary>Task 6 (EP_6)</summary>

```javascript
{{url_alt}}/currency
    req.
    POST
    auth_token
    Resp. Передаётся список массив объектов.
    [
    {"Cur_Abbreviation": str,
    "Cur_ID": int,
    "Cur_Name": str
    }
    …
    {"Cur_Abbreviation": str,
    "Cur_ID": int,
    "Cur_Name": str
    }]
Тесты:
1) Можете взять любой объект из присланного списка, используйте js random.
В объекте возьмите Cur_ID и передать через окружение в следующий запрос.
```

</details>
<details>
<summary>Task 7 (EP_7)</summary>

```javascript
{{url_alt}}/curr_byn
    req.
    POST
    auth_token
    curr_code: int
    Resp.
    {
        "Cur_Abbreviation": str
        "Cur_ID": int,
        "Cur_Name": str,
        "Cur_OfficialRate": float,
        "Cur_Scale": int,
        "Date": str
}
Тесты:
1) Статус код 200
2) Проверка структуры json в ответе.
```

</details>
<details>
<summary>Task 7** (EP_7(js)</summary>

```javascript
1) получить список валют
2) итерировать список валют
3) в каждой итерации отправлять запрос на сервер для получения курса каждой валюты
4) если возвращается 500 код, переходим к следующей итреации
5) если получаем 200 код, проверяем response json на наличие поля "Cur_OfficialRate"
6) если поле есть, пишем в консоль инфу про фалюту в виде response
{
    "Cur_Abbreviation": str
    "Cur_ID": int,
    "Cur_Name": str,
    "Cur_OfficialRate": float,
    "Cur_Scale": int,
    "Date": str
}
7) переходим к следующей итерации
```
</details>
</details>

<details>
<summary> Code </summary>
<details>
<summary>Task 1 (EP_1)</summary>

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// parse token from response
let token = pm.response.json().token
// set token_env var
pm.environment.set("token", token);
```

</details>
<details>
<summary>Task 2 (EP_2)</summary>

```javascript
// 1) Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 2) Проверка структуры json в ответе.
let request_raw = JSON.parse(pm.request.body.raw)
let schema = {
    "type": "object",
    "required": [
        "person",
        "qa_salary_after_12_months",
        "qa_salary_after_6_months",
        "start_qa_salary"
    ],
    "properties": {
        "person": {
            "type": "object",
            "required" : [
                "u_age",
                "u_name",
                "u_salary_1_5_year"
            ],
            "properties":{
                "u_age": {"type" : "integer"},
                "u_name": {"type": "array"},
                "u_salary_1_5_year": {"type": "integer"},
                "u_salary": {"type": "integer"
                }
            }
        },
        "qa_salary_after_12_months": {"type": "number"},
        "qa_salary_after_6_months": {"type": "integer"},
        "start_qa_salary": {"type": "integer"}
    }
}
pm.test("Scheme is correct", function () {
    pm.response.to.have.jsonSchema(schema)
});
// 3) В ответе указаны коэффициенты умножения salary, напишите тесты по проверке правильности результата перемножения на коэффициент.
let respJson = pm.response.json()
pm.test("Server logic (multiplication factor) works ", function () {
        pm.expect(respJson.person.u_salary_1_5_year).to.eql(request_raw.salary*4),
        pm.expect(respJson.start_qa_salary).to.eql(request_raw.salary),
        pm.expect(respJson.qa_salary_after_12_months).to.eql(request_raw.salary*2.9),
        pm.expect(respJson.qa_salary_after_6_months).to.eql(request_raw.salary*2)
});
// 4) Достать значение из поля 'u_salary_1.5_year' и передать в поле salary запроса {{url}}/get_test_user
pm.environment.set("salary_get_test_user", respJson.person.u_salary_1_5_year);
```
</details>
<details>
<summary>Task 3 (EP_3)</summary>

```javascript
// 1) Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 2) Проверка структуры json в ответе.
let schema = {
    "type": "object",
    "requred": [
        "age",
        "name",
        "salary"
    ],
    "properties": {
        "age" : {"type": "integer"},
        "name" : {"type": "string"},
        "salary" : {"type": "array"},
    }
}
pm.test("Scheme is correct", function () {
    pm.response.to.have.jsonSchema(schema)
});
// 3) В ответе указаны коэффициенты умножения salary, напишите тесты по проверке правильности результата перемножения на коэффициент.
let respJson = pm.response.json()
let request_raw = pm.request.body.formdata.get("salary")
pm.test("Server logic (multiplication factor) works ", function () {
        pm.expect(respJson.salary[0]).to.eql+(request_raw.salary),
        pm.expect(respJson.salary[1]).to.eql+(request_raw.salary*2),
        pm.expect(respJson.salary[2]).to.eql+(request_raw.salary*3)
});
// 4) проверить, что 2-й элемент массива salary больше 1-го и 0-го
pm.test("2nd array element > 1 and 0 ", function () {
        pm.expect(respJson.salary[2]).to.gt+(respJson.salary[0])
        pm.expect(+respJson.salary[2]).to.be.above(+respJson.salary[1])
});
```
</details>
<details>
<summary>Task 4 (EP_4)</summary>

```javascript
// 1) Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 2) Проверка структуры json в ответе.
let schema = {
    "type": "object",
    "requred": [
        "age",
        "name",
        "daily_food",
        "daily_sleep"
    ],
    "properties": {
        "age" : {"type": "integer"},
        "name" : {"type": "string"},
        "daily_food" : {"type": "number"},
        "daily_sleep" : {"type": "number"},
    }
}
pm.test("Scheme is correct", function () {
    pm.response.to.have.jsonSchema(schema)
});
// 3) В ответе указаны коэффициенты умножения weight, напишите тесты по проверке правильности результата перемножения на коэффициент.
let respJson = pm.response.json()
let request_raw = pm.request.body.formdata.get("weight")
pm.test("Server logic (multiplication weight factor) works ", function () {
        pm.expect(respJson.daily_food).to.eql(request_raw*0.012),
        pm.expect(respJson.daily_sleep).to.eql(request_raw*2.5)
});
```
</details>
<details>
<summary>Task 5 (EP_5)</summary>

```javascript
// 1) Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 2) Проверка структуры json в ответе.
let schema = {
    "type": "object",
    "requred": [
        "age",
        "family",
        "name",
        "salary"
    ],
    "properties": {
        "age" : {"type": "string"},
        "family" : {"type": "object", "required": ["children", "u_salary_1_5_year" ], "properties": { "children" : { "type": "array"}, "u_salary_1_5_year" : {"type" : "integer"}}},
        "name" : {"type": "string"},
        "salary" : {"type": "integer"},
    }
}
pm.test("Scheme is correct", function () {
    pm.response.to.have.jsonSchema(schema)
});
// 3) Проверить что занчение поля name = значению переменной name из окружения
let respJson = pm.response.json()
// let request_raw = pm.request.body.formdata.get("weight")
pm.environment.set("name", "John");
pm.test("Resp name = var name from env ", function () {
        pm.expect(respJson.name).to.eql(pm.environment.get("name"))
});
// 4) Проверить что занчение поля age в ответе соответсвует отправленному в запросе значению поля age
pm.environment.set("age", 25);
pm.test("Resp age = var age from env ", function () {
        pm.expect(respJson.age).to.eql+(pm.environment.get("age"))
});
```

</details>
<details>
<summary>Task 6 (EP_6)</summary>

```javascript
function getRandomInt(max) {
  return Math.floor(Math.random() * max);
}
var random_num = getRandomInt(118)
// 1) Можете взять любой объект из присланного списка, используйте js random.
// В объекте возьмите Cur_ID и передать через окружение в следующий запрос.
//команда для отладки
// console.log(random_num)
// парсим ответ
let request_info = pm.response.json()
// забираем из ответа нужный рандомный айди
let Info_from_curr = request_info[random_num].Cur_ID
pm.environment.set("Cur_ID", Info_from_curr);
```

</details>
<details>
<summary>Task 7 (EP_7)</summary>

```javascript
// 1) Статус код 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
// 2) Проверка структуры json в ответе.
let scheme = {
    "type": "object",
    "required": [ "Cur_Abbreviation", "Cur_ID", "Cur_Name", "Cur_OfficialRate", "Cur_Scale", "Date"],
    "properties": { "Cur_Abbreviation": {"type" : "string"}, "Cur_ID":{"type":"integer"}, "Cur_Name":{"type":"string"}, "Cur_OfficialRate":{"type":"number"}, "Cur_Scale":{"type":"integer"}, "Date":{"type": "string", "format": "date"}
    }
}
pm.test("Response json scheme is ok", function () {
    pm.response.to.have.jsonSchema(scheme)
});
```

</details>
<details>
<summary>Task 7** (EP_7(js)</summary>

```javascript
// 1) получить список валют
// 2) итерировать список валют
// 3) в каждой итерации отправлять запрос на сервер для получения курса каждой валюты
// 4) если возвращается 500 код, переходим к следующей итреации
// 5) если получаем 200 код, проверяем response json на наличие поля "Cur_OfficialRate"
// 6) если поле есть, пишем в консоль инфу про фалюту в виде response
// {
//     "Cur_Abbreviation": str
//     "Cur_ID": int,
//     "Cur_Name": str,
//     "Cur_OfficialRate": float,
//     "Cur_Scale": int,
//     "Date": str
// }
// 7) переходим к следующей итерации
var info = pm.response.json()
let data1 = info.length
for (var index = 0; index < data1; index++){
    var new_id = info[index].Cur_ID
    var connection = {
    url: pm.environment.get("url_alt")+'/curr_byn',
    method: 'POST',
    header: {'Postman-Token': '23a390b7-9bb2-4ddb-8715-b9d3240a49bd', 
            'Content-Type':'multipart/form-data boundary=--------------------------924870078785244570813508', 
            'Content-Length':'278'}, 
    body: {
        mode: 'formdata',
        formdata: [ {'key': 'auth_token', 'value': 123},
                    {'key': 'curr_code', 'value': new_id}
                 ]
        }
};
     pm.sendRequest(connection, function (err, res) {
                if(res.code == 200){
                var jsonData = res.json();
                    if(pm.expect(jsonData).to.have.any.keys("Cur_OfficialRate")){
                    console.log(jsonData);}
                }})}
```

</details>
</details>





[//]: # (Reference links)
[hw1test_link]: <https://github.com/Foxive/Postman/tree/main/Postman.HW_1.postman_test_run.json>
[hw1col_link]: <https://github.com/Foxive/Postman/tree/main/Postman.HW_1.postman_collection.json>
[hw2test_link]: <https://github.com/Foxive/Postman/tree/main/Postman.HW_2.postman_test_run.json>
[hw2col_link]: <https://github.com/Foxive/Postman/tree/main/Postman.HW_2.postman_collection.json>
[hw2env_link]: <https://github.com/Foxive/Postman/tree/main/HW_2.postman_environment.json>
[hw3col_link]: <https://github.com/Foxive/Postman/tree/main/Postman.HW_3.postman_collection.json>
[hw3test_link]: <https://github.com/Foxive/Postman/tree/main/Postman.HW_3.postman_test_run.json>
[hw3env_link]: <https://github.com/Foxive/Postman/tree/main/HW_3.postman_environment.json>
