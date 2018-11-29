### game RPS
```javascript
function human(){
  var choose = prompt("Введите ваш вариант");
  return choose;
};

function bot(){
   var botChoise = (Math.random() * 100).toFixed(0);
  if(botChoise <= 33){
    botChoise = "Колодец";
    alert("AI выбрал " + botChoise);
    return botChoise;
  } else if(botChoise > 33 && botChoise < 67){
    botChoise = "Ножницы";
    alert("AI выбрал " + botChoise);
    return botChoise;
     }else {
       botChoise = "Бумага";
       alert("AI выбрал " + botChoise);
       return botChoise;
           };
};

function referi(hum, bot){
  var hum1 = hum.toLowerCase();
  var bot1 = bot.toLowerCase();
  if(hum1 == "ножницы" && bot1 == "бумага")return alert("Вы выиграли!");
  if(hum1 == "ножницы" && bot1 == "колодец")return alert("Вы проиграли");
  if(hum1 == "колодец" && bot1 == "ножницы") return alert("Вы выиграли!");
  if(hum1 == "колодец" && bot1 == "бумага") return alert("Вы проиграли");
  if(hum1 == "бумага" && bot1 == "колодец") return alert("Вы выиграли!");
  if(hum1 == "бумага" && bot1 == "ножницы") return alert("Вы проиграли");
 alert("У вас ничья давайте сыграем еще раз");
 return referi(human, bot());
  return alert("У вас ничья давайте сыграем еще раз");
};

referi(human(), bot());
```