# Pizza

Recipe kindly donated by Sam W. <3  
Current status: untasted.


```
function getwarmwater(mug) {
mug.add(water)
while (temp < 45°C) {
mug.heat()
temp = mug.gettemp()
}
mug.add(sugar)
if (temp < 62°) {
return mug
} 
else {
wait()
return mug
}
}

function dryblend(bowl) {
bowl.add(flour)
bowl.add(salt)
bowl.add(fresh_yeast)

while !(yeast_grain_granularity > 0.5mm) {
bowl.mix(grind_between_fingers)
}
return bowl
}

funtion wetblend(bowl, mug) {
bowl.add(mug)
bowl.add(olive_oil)
while (bowl.consistency != homogenous) {
bowl.mix(knead)
}
bowl.coat(more olive oil)
bowl.cover(gladwrap or wet teatowl)
return bowl
}

function main(int pizzas) {
flour = pizzas * 125g
water = pizzas * 75g
yeast = pizzas * 6.25g
salt = pizzas * tiny pinch
olive_oil = pizzas * 5g
mug = getmug()
bowl = getbowl()

bowl = dryblend(bowl)
mug = getwarmwater(mug)
bowl = wetblend(bowl)

pizza_list = {}

risetime = max( 2h, dough doubles in volume)
wait(risetime)

doughballs = bowl.dough.divide_into_balls(pizzas)
wait(1h)

for ball in doughballs {
pizzabase = ball.roll()
pizzabase.add(pasata)
pizzabase.add(toppings)
pizzabase.add(cheese)
pizza = pizzabase.cook(220°, 15-20min)
pizza_list.append(pizza)
}
return pizza_list
}
```
