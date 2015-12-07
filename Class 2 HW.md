1. each row is a new item in an order. each column is a bit of information about the item (the order, quantity, name, notes).
2. 1834 orders
	stss-MacBook-Pro:data Gordon$ tail chipotle.tsv
	1831	1	Carnitas Bowl	[Fresh Tomato Salsa, [Fajita Vegetables, 	Rice, Black Beans, Cheese, Sour Cream, Lettuce]]	$9.25 
	1831	1	Chips	NULL	$2.15 
	1831	1	Bottled Water	NULL	$1.50 
	1832	1	Chicken Soft Tacos	[Fresh Tomato Salsa, [Rice, Cheese, 	Sour Cream]]	$8.75 
	1832	1	Chips and Guacamole	NULL	$4.45 
	1833	1	Steak Burrito	[Fresh Tomato Salsa, [Rice, Black Beans, 	Sour Cream, Cheese, Lettuce, Guacamole]]	$11.75 
	1833	1	Steak Burrito	[Fresh Tomato Salsa, [Rice, Sour Cream, 	Cheese, Lettuce, Guacamole]]	$11.75 
	1834	1	Chicken Salad Bowl	[Fresh Tomato Salsa, [Fajita 		Vegetables, Pinto Beans, Guacamole, Lettuce]]	$11.25 
	1834	1	Chicken Salad Bowl	[Fresh Tomato Salsa, [Fajita 		Vegetables, Lettuce]]	$8.75 
	1834	1	Chicken Salad Bowl	[Fresh Tomato Salsa, [Fajita 		Vegetables, Pinto Beans, Lettuce]]	$8.75
3. 4623 lines
	stss-MacBook-Pro:data Gordon$ wc -l chipotle.tsv
    	4623 chipotle.tsv
4. 553 chicken burritos ordered v 368 steak burritos ordered, Chicken
	stss-MacBook-Pro:data Gordon$ grep -i 'chicken burrito' chipotle.tsv | wc -l
     	553
	stss-MacBook-Pro:data Gordon$ grep -i 'steak burrito' chipotle.tsv | wc -l
     	368
5. 282 chicken burritos with black beans v 105 chicken burritos with pinto beans, black
6. stss-MacBook-Pro:DAT-DC-10 Gordon$ find . -name "*sv"
./data/airlines.csv
./data/bank-additional.csv
./data/bikeshare.csv
./data/chipotle.tsv
./data/drinks.csv
./data/hitters.csv
./data/imdb_1000.csv
./data/sms.tsv
./data/titanic.csv
./data/ufo.csv
./data/vehicles_test.csv
./data/vehicles_train.csv
./data/yelp.csv
7. “dictionary” is used 91 times
	stss-MacBook-Pro:DAT-DC-10 Gordon$ grep -i "dictionary" . | wc -l
	grep: .: Is a directory
       	0
	stss-MacBook-Pro:DAT-DC-10 Gordon$ grep -ir "dictionary" . | wc -l
      	91
8. Bowls are more popular than burritos (1311 bowls v 1172 burritos)
	stss-MacBook-Pro:data Gordon$ grep -i "bowl" chipotle.tsv | wc -l
    	1331
	stss-MacBook-Pro:data Gordon$ grep -i "burrito" chipotle.tsv | wc -l
    	1172
