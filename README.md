#Page 1
---
		## What Flexbox is?

		- A new CSS layout system that makes it easy to build dynamic layouts. 						


#Page 2
---
		## Why use Flexbox?

		- Vertical centering
		- Reordering								
		- Allow we do not use float or table anymore 


#Page 3
---
		## When can i use Flexbox?
		
		- Now!
		- Now has supportted almost 94% browsers [http://caniuse.com/#search=flex](http://caniuse.com/#search=flex)


#Page 4
---
		### How to use Flexbox?
		
		- Let's make a simple example to use it!
		
		![dices](./assets/all-faces.png)

#Page 5: Dice One
---
##5-1
---
			###Dice: One

			![dices](./assets/face-1-1.png)

			```
				<div class="first-face">
				  <span class="dot"></span>
				</div>
			```

##5-2
---
			###justify-content: center

			![dices](./assets/face-1-2.png)

			```
				.first-face {
				  display: flex;

				  justify-content: center;
				}
			```

##5-3
---
			###align-items: center

			![dices](./assets/face-1-3.png)

			```
				.first-face {
				  display: flex;

				  justify-content: center;
 
				  align-items: center;
				}
			```
#Page 6: Dice Two
---
##6-1
---
			###Dice: Two

			![dices](./assets/face-2-1.png)

			```
				<div class="second-face">
				  <span class="dot"></span>
				  <span class="dot"></span>
				</div>
			```

##6-2
---
			###justify-content: space-between

			![dices](./assets/face-2-2.png)

			```
				.second-face {
				  display: flex;
				  justify-content: space-between;
				}
			```

##6-3
---
			###align-self: flex-end

			![dices](./assets/face-2-3.png)

			```
				.second-face {
				  display: flex;
				  justify-content: space-between;
				}

				.second-face .dot:nth-of-type(2) {
				  align-self: flex-end;
				}
			```
#Page 7: Dice Three
---
##7-1
---
			###Dice: Three

			![dices](./assets/face-3-1.png)

			```
				<div class="third-face">
				  <span class="dot"></span>
				  <span class="dot"></span>
				  <span class="dot"></span>
				</div>
			```

##7-2
---
			###align-self: center

			![dices](./assets/face-3-2.png)

			```
				.third-face {
				  display: flex;
				  justify-content: space-between;
				}

				.third-face .dot:nth-of-type(2) {
				  align-self: center;
				}
			```

##7-3
---
			###align-self: flex-end

			![dices](./assets/face-3-3.png)

			```
				.third-face {
				  display: flex;
				  justify-content: space-between;
				}

				.third-face .dot:nth-of-type(2) {
				  align-self: center;
				}

				.third-face .dot:nth-of-type(3) {
				  align-self: flex-end;
				}
			```
#Page 8: Dice Four
---
##8-1
---
			###Dice: Four

			![dices](./assets/face-4-1.png)

			```
				<div class="fourth-face">
					<div class="face-column">
					  <span class="dot"></span>
					  <span class="dot"></span>
					</div>
					<div class="face-column">
					  <span class="dot"></span>
					  <span class="dot"></span>
					</div>
				</div>
			```

##8-2
---
			###justify-content: space-between

			![dices](./assets/face-4-2.png)

			```
				.fourth-face {
				  display: flex;
				  justify-content: space-between;
				}
			```

##8-2-alert
---
			###highlight face-column

			![dices](./assets/face-4-2-alert.png)
			
			```
				<div class="fourth-face">
					<div class="face-column" style="outline: 1px solid red">
					  <span class="dot"></span>
					  <span class="dot"></span>
					</div>
					<div class="face-column" style="outline: 1px solid red">
					  <span class="dot"></span>
					  <span class="dot"></span>
					</div>
				</div>
			```

##8-3-alert
---
			###nested flexbox

			![dices](./assets/face-4-3-alert.png)

			```
				.fourth-face {
				  display: flex;
				  justify-content: space-between;
				}

				.fourth-face .face-column {
				  display: flex;
				  /* default 
				  	flex-direction: row; // left to right 
				  */
				}
			```

##8-4
---
			###nested flexbox

			![dices](./assets/face-4-3.png)

			```
				.fourth-face {
				  display: flex;
				  justify-content: space-between;
				}

				.fourth-face .face-column {
				  display: flex;
				  flex-direction: column; // top to bottom
				  justify-content: space-between; 
				}
			```
#Page 9: Dice Five
---
##9-1
---
			###Dice: Five

			![dices](./assets/face-5-1.png)

			```
				<div class="fifth-face">
				  <div class="column">
				    <span class="dot"></span>
				    <span class="dot"></span>
				  </div>
				  <div class="column">
				    <span class="dot"></span>
				  </div>
				  <div class="column">
				    <span class="dot"></span>
				    <span class="dot"></span>
				  </div>
				</div>
			```

##9-2
---
			###Dice: Five

			![dices](./assets/face-5-2.png)

			```
				.fifth-face {
				  display: flex;
				  justify-content: space-between;
				}
				  
				.fifth-face .column {
				  display: flex;
				  flex-direction: column;
				  justify-content: space-between;
				}
			```

##9-3
---
			###Dice: Five

			![dices](./assets/face-5-3.png)

			```
				.fifth-face {
				  display: flex;
				  justify-content: space-between;
				}
				  
				.fifth-face .column {
				  display: flex;
				  flex-direction: column;
				  justify-content: space-between;
				}
				  
				.fifth-face .column:nth-of-type(2) {
				  justify-content: center;
				}
			```
#Page 10: Dice Six
---
##10-1
---
			###Dice: Six

			![dices](./assets/face-6-1.png)

			```
				<div class="sixth-face">
				  <div class="column">
				    <span class="dot"></span>
				    <span class="dot"></span>
				    <span class="dot"></span>
				  </div>
				  <div class="column">
				    <span class="dot"></span>
				    <span class="dot"></span>
				    <span class="dot"></span>
				  </div>
				</div>
			```

##10-2
---
			###Dice: Six

			![dices](./assets/face-6-2.png)

			```
				.sixth-face {
				  display: flex;
				  justify-content: space-between;
				}
				  
				.sixth-face .column {
				  display: flex;
				  flex-direction: column;
				  justify-content: space-between;
				}
			```