# JavaScriptVerkefni2

**2.1**<br/>
1. **Afhverju er getElementById() fljótleglegasta aðferðin?**<br/>
   getElementById is direct call to the JavaScript engine and returns a DOM object.

2. **Hver er munurinn á static og live NodeList?**<br/>
   A live nodelist is in the Dom while a static one is not.

3. **Hver er munurinn á true og false í AddEventListener?**<br/>
   true og false í AddEventListener ræður um hvort þú vilt nota useCapture eða ekki.
   
4. **this vísar í Event listener á html element en ekki á object. Þú getur notað bind() til að breyta því. Leystu eftirfarandi kóðadæmi      með notkun á bind() til að birta í console “My name is Sam“ en ekki undefined.**<br/>
   ```javascript
   let Person = {
	 name: "Sam",
	 sayName: function(){
		 console.log("my name is "+ this.name));
	 }
	 };
	 buttonE1.addEventListener("click", Person.sayName.bind(Person)); 
   ```
**2.2**<br/>
1. **Notaðu querySelector() til að velja málsgrein nr 1. og litaðu textann rauðan.**<br/>
   ```javascript 
   document.querySelector("p").style.color = "red"; 
   ```
2. **Veldu allar málgreinar og breyttu textanum í ensku með textContent aðferðinni.**<br/>
   ```javascript 
   let allP = document.querySelectorAll("p");
   for (let i = 0; i < allp.length; i++) {
       allp[i].document.textContent = "paragraph";
   }
   document.querySelector("div > p").textContent = "paragraph";
   ```
3. **Bættu við efst með InnerHTML h1 með textanum Verkefni 2.2.**<br/>
   ```javascript 
   let htmlContent = document.body.innerHTML;
   document.body.innerHTML = <h1>Verkefni 2</h1> + htmlContent;
   ```
4. **Bættu við neðst með createElement() og append() málsgrein með nafninu þínu.**<br/>
   ```javascript 
   let newElement = document.createElement("p");
   newElement.innerHTML = "Haukur";
   document.body.appendChild(newElement);
   ```
