<!-- Page 1 -->
<section data-markdown>
	<script type="text/template">
		## What Flexbox is?

		- A new CSS layout system that makes it easy to build dynamic layouts. 						
	</script>
</section>


<!-- Page 2 -->
<section data-markdown>
	<script type="text/template">
		## Why use Flexbox?

		- Vertical centering
		- Reordering								
		- Allow we do not use float or table anymore 
	</script>
</section>


<!-- Page 3 -->
<section data-markdown>
	<script type="text/template">
		## When can i use Flexbox?
		
		- Now!
		- Now has supportted almost 94% browsers [http://caniuse.com/#search=flex](http://caniuse.com/#search=flex)
	</script>
</section>


<!-- Page 4 -->
<section data-markdown>
	<script type="text/template">
		### How to use Flexbox?
		
		- Let's make a simple example to use it!
		
		![dices](./assets/all-faces.png)
	</script>
</section>

<!-- Page 5: Dice One -->
<section>
	<!-- 5-1 -->
	<section data-markdown>
		<script type="text/template">
			###Dice: One

			![dices](./assets/face-1-1.png)

			```
				<div class="first-face">
				  <span class="dot"></span>
				</div>
			```
		</script>
	</section>

	<!-- 5-2 -->
	<section data-markdown>
		<script type="text/template">
			###justify-content: center

			![dices](./assets/face-1-2.png)

			```
				.first-face {
				  display: flex;

				  justify-content: center;
				}
			```
		</script>
	</section>

	<!-- 5-3 -->
	<section data-markdown>
		<script type="text/template">
			###align-items: center

			![dices](./assets/face-1-3.png)

			```
				.first-face {
				  display: flex;

				  justify-content: center;
 
				  align-items: center;
				}
			```
		</script>
	</section>
</section>

<!-- Page 6: Dice Two -->
<section>
	<!-- 6-1 -->
	<section data-markdown>
		<script type="text/template">
			###Dice: Two

			![dices](./assets/face-2-1.png)

			```
				<div class="second-face">
				  <span class="dot"></span>
				  <span class="dot"></span>
				</div>
			```
		</script>
	</section>

	<!-- 6-2 -->
	<section data-markdown>
		<script type="text/template">
			###justify-content: space-between

			![dices](./assets/face-2-2.png)

			```
				.second-face {
				  display: flex;
				  justify-content: space-between;
				}
			```
		</script>
	</section>

	<!-- 6-3 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>
</section>

<!-- Page 7: Dice Three -->
<section>
	<!-- 7-1 -->
	<section data-markdown>
		<script type="text/template">
			###Dice: Three

			![dices](./assets/face-3-1.png)

			```
				<div class="third-face">
				  <span class="dot"></span>
				  <span class="dot"></span>
				  <span class="dot"></span>
				</div>
			```
		</script>
	</section>

	<!-- 7-2 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>

	<!-- 7-3 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>
</section>

<!-- Page 8: Dice Four -->
<section>
	<!-- 8-1 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>

	<!-- 8-2 -->
	<section data-markdown>
		<script type="text/template">
			###justify-content: space-between

			![dices](./assets/face-4-2.png)

			```
				.fourth-face {
				  display: flex;
				  justify-content: space-between;
				}
			```
		</script>
	</section>

	<!-- 8-2-alert -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>

	<!-- 8-3-alert -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>

	<!-- 8-4 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>
</section>

<!-- Page 9: Dice Five -->
<section>
	<!-- 9-1 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>

	<!-- 9-2 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>

	<!-- 9-3 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>
</section>

<!-- Page 10: Dice Six -->
<section>
	<!-- 10-1 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>

	<!-- 10-2 -->
	<section data-markdown>
		<script type="text/template">
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
		</script>
	</section>
</section>