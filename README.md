# javascriptstudy
// Defintions 
var javaScriptDefine, variableDefine, numberDefine,stringDefine, booleansDefine, arraysDefine, objectDefine, pushDefine, popDefine, unshiftDefine, shiftDefine,switchStatementDefine,ternaryDefine, joinDefine,splitDefine, parseDefine,stringifyDefine;
javaScriptDefine = "JavaScript is a programming language that allows you to implement complex things on web pages — every time a web page does more than just sit there and display static information for you to look at — displaying timely content updates, or interactive maps, or animated 2D/3D graphics, or scrolling video jukeboxes, etc. ";
variableDefine = "A variable is a container for a value, like a number we might use in a sum, or a string that we might use as part of a sentence.";
numberDefine = "You can store numbers in variables, be those whole numbers like 30 (also called integers) or decimal numbers like 2.456 (also called floats or floating point numbers).";
stringDefine = "Strings are pieces of text. When you give a variable a string value, you need to wrap it in single or double quote marks, otherwise JavaScript will try to intepret it as another variable name.";
booleansDefine = "Booleans are true/false values — they can have two values, true or false. These are generally used to test a condition, after which code is run as appropriate. ";
arraysDefine ="An array is a single object that contains multiple values enclosed in square brackets and separated by commas.";
objectDefine = "In programming, an object is a structure of code that models a real life object. You can have a simple object that represents a car park and contains information about its width and length, or you could have an object that represents a person";
pushDefine = "add item to an arrayat the end";
popDefine = "remove item from the end of an array";
splitDefine ="when taking a string, and using this method to convert it to an array";
joinDefine ="creating a string from an array";
unshiftDefine = "add item to feont of an Array";
shiftDefine ="remove item in front of an Array"
switchStatementDefine = "hey take a single expression/value as an input, and then look through a number of choices until they find one that matches that value, executing the corresponding code";
ternaryDefine = "if else steatment without the need of a block but a one line statment";
parseDefine = "Accepts a JSON object in text string form as a parameter, and returns the corresponding object.";
stringifyDefine = "Accepts a JSON object as a parameter, and returns the equivalent text string form.";
// variable examples
var numberVar, stringVar, booleanVar, arrayVar, arrayAcessVar, objectVar, objectAcessVar;
numberVar = 16;
stringVar = "JavaScript";
booleanVar = true;
arrayVar = ['Developer, Programmer, Engineer'];
arrayAcessVar = arrayVar[0];
objectVar = {
    name:'Victor',
    age: '23',
    weight: '205'
}
objectAcessVar = objectVar.name;

// array examples
var shoppingArrayExp = ['bread','milk','cheese', 'humouns', 'noodles'];
var shoopingArrayAcess = shoppingArrayExp[0];
var multiArrayExp = ['tree',4,[0,1,2]];
var multiArrayAcess = [2][2];

// finding the length of an array using a for loop
var sequenceExp = [1, 1, 2, 3, 5, 8, 13];
sequenceExp.length;
for(var i = 0; i < sequenceExp.length; i++){
   sequenceExp[i]; // display list of sequenceExp
}
// converting from strings and array 
var stringToArrayExp = 'Manchester,London,Liverpool,Birmingham,Leeds,Carlisle';
var arrayFromString = stringToArrayExp.split(',');
// creating a string from a an array 
var arrayToString = arrayFromString.join(',');
//adding and removing items in a array
var addRemoveArray = ['Manchester', 'London', 'Liverpool', 'Birmingham', 'Leeds', 'Carlisle'];
addRemoveArray.push("Chicago");
addRemoveArray.pop("");
addRemoveArray.unshift();
addRemoveArray.shift();
// if else if click event triggered by a change method that automatically updates things
var select = document.querySelector('select');//this is a form option drop down
var para = document.querySelector('p');

select.addEventListener('change', setWeather); //cretes the change and activates this function

function setWeather() {
  var choice = select.value; //this takes the value set in the HTML option container, by using 'value'

  if (choice === 'sunny') {//chocice === 'this is the value set in the HTML'
    para.textContent = 'It is nice and sunny outside today. Wear shorts! Go to the beach, or the park, and get an ice cream.';
  } else if (choice === 'rainy') {
    para.textContent = 'Rain is falling outside; take a rain coat and a brolly, and don\'t stay out for too long.';
  } else if (choice === 'snowing') {
    para.textContent = 'The snow is coming down — it is freezing! Best to stay in with a cup of hot chocolate, or go build a snowman.';
  } else if (choice === 'overcast') {
    para.textContent = 'It isn\'t raining, but the sky is grey and gloomy; it could turn any minute, so take a rain coat just in case.';
  } else {
    para.textContent = '';
  }
}
// Nesting if ... else 
if (choice === 'sunny') {
  if (temperature < 86) {
    para.textContent = 'It is ' + temperature + ' degrees outside — nice and sunny. Let\'s go out to the beach, or the park, and get an ice cream.';
  } else if (temperature >= 86) {
    para.textContent = 'It is ' + temperature + ' degrees outside — REALLY HOT! If you want to go outside, make sure to put some suncream on.';
  }
}
//Using && AND or || OR
if (choice === 'sunny' && temperature < 86) {
  para.textContent = 'It is ' + temperature + ' degrees outside — nice and sunny. Let\'s go out to the beach, or the park, and get an ice cream.';
} else if (choice === 'sunny' || temperature >= 86) {
  para.textContent = 'It is ' + temperature + ' degrees outside — REALLY HOT! If you want to go outside, make sure to put some suncream on.';
}
// Switch statement examples
var select = document.querySelector('select');//select HTML form
var para = document.querySelector('p');//place it on the page

select.addEventListener('change', setWeather);//when select is changed do this function

function setWeather() { //function name
  var choice = select.value;//selecting the name of the HTML value in the option HTML aka select

  switch (choice) {//value is == to choice 
    case 'sunny'://value name
      para.textContent = 'It is nice and sunny outside today. Wear shorts! Go to the beach, or the park, and get an ice cream.';
      break;
    case 'rainy':
      para.textContent = 'Rain is falling outside; take a rain coat and a brolly, and don\'t stay out for too long.';
      break;
    case 'snowing':
      para.textContent = 'The snow is coming down — it is freezing! Best to stay in with a cup of hot chocolate, or go build a snowman.';
      break;
    case 'overcast':
      para.textContent = 'It isn\'t raining, but the sky is grey and gloomy; it could turn any minute, so take a rain coat just in case.';
      break;
    default:
      para.textContent = '';
  }
}
// ternary exmample 
var ternaryExp = ( isBirthday ) ? 'Happy birthday Mrs. Smith — we hope you have a great day!' : 'Good morning Mrs. Smith.';

// Looping tthrough an array to output
var cats = ['Bill', 'Jeff', 'Pete', 'Biggles', 'Jasmin'];//array
var info = 'My cats are called ';
var para = document.querySelector('p');

for (var i = 0; i < cats.length; i++) {
  info += cats[i] + ', ';
}
para.textContent = info;

// Looping through list of contact people through a input form
var contacts = ['Chris:2232322', 'Sarah:3453456', 'Bill:7654322', 'Mary:9998769', 'Dianne:9384975'];
var para = document.querySelector('p');
var input = document.querySelector('input');
var btn = document.querySelector('button');

btn.addEventListener('click', function() {
  var searchName = input.value; //input form serach for value
  input.value = ''; //clearing out input form when clicked
  input.focus();
  for (var i = 0; i < contacts.length; i++) {
    var splitContact = contacts[i].split(':');
    if (splitContact[0] === searchName) {
      para.textContent = splitContact[0] + '\'s number is ' + splitContact[1] + '.';
      break;
    } else {
      para.textContent = 'Contact not found.';
    }
  }
});

// Object in javascript 
var person = {
  name: ['Bob', 'Smith'],
  age: 32,
  gender: 'male',
  interests: ['music', 'skiing'],
  bio: function() {
    alert(this.name[0] + ' ' + this.name[1] + ' is ' + this.age + ' years old. He likes ' + this.interests[0] + ' and ' + this.interests[1] + '.');
  },
  greeting: function() {
    alert('Hi! I\'m ' + this.name[0] + '.');
  }
};
// construstor function 
function Person(first, last, age, gender, interests) {
  this.name = {
    first,
    last
  };
  this.age = age;
  this.gender = gender;
  this.interests = interests;
  this.bio = function() {
    alert(this.name.first + ' ' + this.name.last + ' is ' + this.age + ' years old. He likes ' + this.interests[0] + ' and ' + this.interests[1] + '.');
  };
  this.greeting = function() {
    alert('Hi! I\'m ' + this.name.first + '.');
  };
};
// calling a constructor to create a new object of it 
var person1 = new Person('Bob', 'Smith', 32, 'male', ['music', 'skiing']);
person1['age']
person1.interests[1]
person1.bio();
