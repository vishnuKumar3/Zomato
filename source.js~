var check=[0,0,0,0,0];
var itemsAll={
	0:[
		"images/food.webp",
		"Daryaganj-By the inventors of Butter chicken and dal mackani",
		"4.3",
		"(367 Delivery Reviews)",
		"North Indian, Mughlai, Desserts, Seafood, Kebab, Biryani",
		"Connaught Place",
		"12:30pm – 12midnight (Today)",
		"450 for one . 29min",
		"Promoted",
		"background:linear-gradient(to right,red 20%,rgb(207,207,207) 1%)",
		"Rating:4.0+ Pure veg Safe and hygenic Great offers Rating:4.0+"	
	],
	1:[
		"images/food2.webp",
		"Domino's Pizza",
		"4.8",
		"(500 Delivery Reviews)",
		"Pizza fast food",
		"Connaught",
		"12:30pm – 12midnight (Today)",
		"150 for one . 30min",
		"",
		"background:linear-gradient(to right,red 80%,rgb(207,207,207) 1%)",
		"Safe and hygenic Great offers Rating:4.0+"		
	],
	2:[
		"images/food3.webp",
		"Karim's",
		"4.0",
		"(120 Delivery Reviews)",
		"Rolls North Indian, Mughlai",
		"Connaught Place",
		"12:30pm – 12midnight (Today)",
		"300 for one . 50min",
		"Promoted",
		"background:linear-gradient(to right,red 0%,rgb(207,207,207) 1%)",
		"Rating:4.0+ Delivery time"		
	],
	3:[
		"images/food4.webp",
		"Spice Market",
		"4.0",
		"(500 Delivery Reviews)",
		"North Indian, Mughlai, Beverages, Biryani, Hyderabadi",
		"Greater Kailash 1 (GK1)",
		"11:30am – 1am (Today)",
		"350 for one . 50min",
		"Promoted",
		"background:linear-gradient(to right,red 0%,rgb(207,207,207) 1%)",
		"Rating:4.0+ Safe and hygenic Great offers"		
	],
	4:[
		"images/food6.webp",
		"Bikanervala",
		"4.3",
		"(350 Delivery Reviews)",
		"Mithai, North Indian, South Indian, Chinese, Fast Food, Street Food, Desserts, Beverages",
		"Connaught Place",
		"9am – 10pm (Today)",
		"100 for one . 25min",
		"",
		"background:linear-gradient(to right,red 30%,rgb(207,207,207) 1%)",
		"Rating:4.0+ Pure veg"		
	],
	5:[
		"images/food5.webp",
		"Chickeera",
		"4.8",
		"(200 Delivery Reviews)",
		"American, Mexican, Lebanese, Tex-Mex",
		"South Extension 1",
		"12noon – 5am (Today)",
		"400 for one . 36min",
		"Promoted",
		"background:linear-gradient(to right,red 80%,rgb(207,207,207) 1%)",
		"Rating:4.0+ Great offers"		
	]


	};


window.onload=displayItems(itemsAll);


function searchFun(){
var val=document.getElementById("searchBox").value;
if(val.length>0){
	var newItems={};
	var index=0;
	for(i=0;i<6;i++){
		if(itemsAll[i][1].includes(val)) {
			newItems[index]=itemsAll[i];
			index++;
		}
	}
	displayItems(newItems);
}
else{
	displayItems(itemsAll)
}
}


function displayItems(totalItems){
document.title="Delhi NCR restaurants,Restaurants in Delhi NCR-Zomato";

var items={};
items=totalItems;
console.log(items);

var text="";
for(i=0;i<Object.keys(items).length;i++){
text+='<div id="card">'+
'<div id="img">'+
`<img style="border-radius:10px 10px 0px 0px;width:100%;height:100%;" src="${items[i][0]}"/>`+
'</div>'+
'<li id="heading">'+
`${items[i][1]}`+
'</li>'+

'<div id="ratingBox">'+
'<div id="leftBox">'+
'<div class="rating">'+
'<i class="fa fa-star" style="font-size:16px;color:white;"></i>'+
'</div>'+
'<div class="rating">'+
'<i class="fa fa-star" style="font-size:16px;color:white;"></i>'+
'</div>'+
'<div class="rating">'+
'<i class="fa fa-star" style="font-size:16px;color:white;"></i>'+
'</div>'+
'<div class="rating">'+
'<i class="fa fa-star" style="font-size:16px;color:white;"></i>'+
'</div>'+
`<div style="${items[i][9]}" class="rating">`+
'<i class="fa fa-star" style="font-size:16px;color:white;"></i>'+
'</div>'+
`<div style="margin-left:2%;">${items[i][2]}</div>`+
'</div>'+

'<div id="rightBox">'+
`<li id="delivery">${items[i][3]}</li>`+
'</div>'+
'</div>'+

`<li id="details1">${items[i][4]}</li>`+
`<li id="details2">`+
`${items[i][5]}<br/>`+
`${items[i][6]}<br/>`+
`${items[i][7]}`+
'</li>'+
`<li id="details3">${items[i][8]}</li>`+
'</div>';
}
document.getElementById("mainBody").innerHTML=text;

}


function filters(event){
var indexCheck=parseInt(event.target.id);
check[indexCheck]+=1;
var button=document.getElementById(event.target.id);

if(check[indexCheck]%2==1){
button.style.background="black";
button.style.color="white";
var filterVar=event.target.id.slice(1).toString();
var newItems={};
var index=0;
for(i=0;i<6;i++){
	if(itemsAll[i][10].includes(filterVar)){
		newItems[index]=itemsAll[i];
		index++;
	}	
	}
		displayItems(newItems);
}

else{
	button.style.background="white";
	button.style.color="black";
	displayItems(itemsAll);
}

}

