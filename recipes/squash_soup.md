# Squash soup

- [x] Vegan
- Difficulty: Easy
- Time: 1h

### Ingredients

- Squash  
- White onion
- Garlic
- Water || Veggie Stock  
- Salt  
- Pepper
- Chilli (optional)
- Grana padano (optional)
- Olive oil  

### Make and bake

```javascript
var fullSquash = "squashskin"
var fullOnion = "onionskin"
var fullGarlic = "garlicskin"
var oil = "oil"
var veggieStock = "enough to cover"
var salt = "enough for taste"
var pepper = "enough for taste"
var bravery = Math.floor(Math.random() * 100) + 1;

function peel(ingredient) {
  return ingredient.split('skin')[0];
}

function chop(ingredient) {
  if (Math.floor(Math.random() * 100) + 1 > 90) {
  	alert("!!!Carefull, you almost shopped yourself!!!")
  }

	return ingredient.split('');
}

function boil(ingredient, liquid) {
 return ingredient+liquid+"boiled"
}

function blend(ingredients) {
	if (ingredients.endsWith("boiled")) {
  	return "soup";
  }

	return "mash"
}

function cook(ingredient) {
	return ingredient+"cooked"
}

function stir(ingredient) {
	return ingredient
  				.split("")
          .reverse()
          .join("")
}


function feelingBrave(ingredients, bravery) {
result = ""
var bravery = parseInt(bravery);
switch (true) {
    case bravery < 25:
       result = ingredients + "spicy"
      break;
    case bravery < 50:
       result = ingredients + "nice touch"
      break;
    case bravery < 70:
       result = ingredients + "nice touch,your majesty"
      break;
    case bravery < 85:
       result = ingredients + "get a napkin for the sweat"
      break;
    case bravery < 95:
       result = ingredients + "Tastebuds? Hello? Hello? Are you there...."
      break;
    case bravery < 100:
       result = ingredients + "This is going to burn twice..."
      break;
	}

  return result
}

console.log("Preparation");
var skinLessSquash = peel(fullSquash);
var choppedSquash = chop(skinLessSquash);

var skinLessOnion = peel(fullOnion);
var choppedOnion = chop(skinLessOnion);


var skinLessGarlic = peel(fullGarlic);
var choppedGarlic = chop(skinLessGarlic);

var pot = ""
pot += oil

console.log("Let's begin")
var m = cook(pot+choppedGarlic+choppedOnion)
var mm = stir(m)
var mmm = cook(mm)
var mmmm = stir(mmm)

console.log("Getting there")
var mmmmm = feelingBrave(mmmm, bravery)
var mmmmmm = boil(mmmmm+choppedSquash, veggieStock)
var mmmmmmm = blend(mmmmmm)

if (mmmmmmm == "soup") {
	alert("Enjoy !!!!!!");
}

```

## Side notes
Add amount of ingredients depending on how many people you want a feed :)
Fine tunning of the amounts might require multiple iterations of this recipe.

PS: For the lolz, run the script on a browser :)
