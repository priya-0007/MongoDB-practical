# MongoDB-practical
**************************************************
### MongoDB Practical Slip Solution
#### Slip 1
#### 2) And 3)=>
````
>
db.student.insert({name:"Abhi",course:[{coursename:"bcs"},
{
coursename:"bvoc"}],marks:80,age:21,gender:"male",city:"p
une"})
WriteResult({ "nInserted" : 1 })
>
db.student.insert({name:"mukesh",course:[{coursename:"bc
s
"},{coursename:"bvoc"}],marks:60,age:22,gender:"male",cit
y:
"pune"})
WriteResult({ "nInserted" : 1 })
>
db.student.insert({name:"manisha",course:[{coursename:"m
cs"},{coursename:"bvoc"}],marks:90,age:22,gender:"female
",city:"mumbai"})
WriteResult({ "nInserted" : 1 })
>
db.student.insert({name:"manasi",course:[{coursename:"mc
s"},{coursename:"bvoc"}],marks:92,age:22,gender:"female",
city:"latur"})
WriteResult({ "nInserted" : 1 })
>
db.student.insert({name:"apurva",course:[{coursename:"mc
s"},{coursename:"bvoc"}],marks:37,age:22,gender:"female",
city:"sasvad"})
WriteResult({ "nInserted" : 1 })
>
db.student.insert({name:"arati",course:[{coursename:"mcs"}
,
{coursename:"bvoc"}],marks:32,age:22,gender:"female",city
:"bekarai"})
WriteResult({ "nInserted" : 1 })
````
#### 4)=>
#### a)
````
 > db.student.count({marks:{$gt:80}})
````
#### b)
````
 > db.student.find({marks:{$lt:40}})
````
#### c)
````
 > var my=db.student.find({marks:{$gt:70}});
> while(my.hasNext()){print(tojson(my.next()));}
````
#### d)
````
>db.student.find({gender:"female",$or:[{city:"pune"},{city:"
mumbai"},{marks:{$lt:50}}]})
````
**************************************************
#### slip 2
#### 2) &3)=>
````
> db.product.insert({name:"robot",price:12000})
WriteResult({ "nInserted" : 1 })
> db.product.insert({name:"toycar",price:2000})
WriteResult({ "nInserted" : 1 })
> db.product.insert({name:"cricketset",price:9000})
WriteResult({ "nInserted" : 1 })
> db.product.insert({name:"studymaterial",price:19000})
WriteResult({ "nInserted" : 1 })
> db.order.insert({orderno:3736,custName:"arun
kumar",product:{productName:"toycar",price:20000},order_
date:"12/2/2019",stetus:"processed",Totalbill:2039,invoice:{i
nvoiceNO:67564,bill:2039,date:"17/2/2019"}})
WriteResult({ "nInserted" : 1 })
> db.order.insert({orderno:3737,custName:"arun
kumar",product:{productName:"robot",price:12000},order_d
ate:"11/3/2019",stetus:"processed",Totalbill:12800,invoice:{i
nvoiceNO:67574,bill:12039,date:"17/3/2019"}})
WriteResult({ "nInserted" : 1 })
> db.order.insert({orderno:3738,custName:"arun
kumar",product:{productName:"cricketset",price:9000},order
_date:"15/5/2019",stetus:"in process",Totalbill:9050})
WriteResult({ "nInserted" : 1 })
> db.order.insert({orderno:3739,custName:"mukesh
patil",product:{productName:"studentmaterial",price:19000}
,order_date:"15/8/2019",stetus:"in process",Totalbill:19080})
WriteResult({ "nInserted" : 1 })
````
#### 4)
#### a)
````
> db.product.find().pretty()
````
#### b)
````
 > db.order.find({Totalbill:{$lt:10000}})
````
#### c)
````
 > db.order.find({stetus:"in process"})
````
#### d)
```` >db.order.find({custName:"arun
kumar",stetus:"processed"})
````
**************************************************
#### slip 3
#### 2)&3)=>
````
> db.book.insert({BName:"shyamchi
aai",cost:700,author:"sane guruji",published:2007})
WriteResult({ "nInserted" : 1 })
> db.book.insert({BName:"Two
Saints",cost:1700,author:"raguramkrishna",published:2017})
WriteResult({ "nInserted" : 1 })
> db.book.insert({BName:"ramkrushna
paramhans",cost:800,author:"raguramkrishna",published:20
17})
WriteResult({ "nInserted" : 1 })
>
db.book.insert({BName:"DMS",cost:300,author:"raguramkri
shna",published:2005})
WriteResult({ "nInserted" : 1 })
> db.publisher.insert({pname:"O
Reilly",language:"English",books:[{BName:"ramkrushna
paramhans"},{BName:"Two Saints"}],city:"mumbai"})
WriteResult({ "nInserted" : 1 })
>
db.publisher.insert({pname:"vision",language:"English",boo
ks:[{BName:"DMS"}],city:"pune"})
WriteResult({ "nInserted" : 1 })
> db.publisher.insert({pname:"O
Reilly",language:"marathi",books:[{BName:"shyamchi
aai"}],city:"mumbai"})
WriteResult({ "nInserted" : 1 })
````
#### 4)
#### a)
````
> db.publisher.find({city:"mumbai"})
````
#### b)
````
> db.book.find({cost:{$lt:1000}})
````
#### c)
````
 >
db.book.find({author:"raguramkrishna",published:2017})
````
#### d)
````
 > db.publisher.find({pname:"O
Reilly",$or:[{language:"English"},{language:"marathi"}]})
````
**************************************************
#### slip 4
#### 2)&3)=>
````
>
db.Hospital.insert({Hno:1,Hname:"AAA",Specialization:["Pe
diatric","Gynaec","Orthopaedic"],People:[{Pname:"PQR",Ra
ting:4},{Pname:"SDE",Rating:5}],Doctor:[{"Dname" :
"WWW","Visit" : "Sunday"}]})
WriteResult({ "nInserted" : 1 })
>
db.Hospital.insert({Hno:2,Hname:"BBB",Specialization:["Gy
naec","Orthopaedic"],People:[{Pname:"POP",Rating:2},{Pna
me:"SDE",Rating:3}],Doctor:[{"Dname":"XXX",Visit:"Monday
"}]})
WriteResult({ "nInserted" : 1 })
>
db.Hospital.insert({Hno:3,Hname:"CCC",Specialization:["Gy
naec","Orthopaedic","Pediatric"],People:[{Pname:"KLO",Rat
ing:3},{Pname:"LPO",Rating:3}],Doctor:[{"Dname" :
"XXX","Visit":"Tuesday"}]})
WriteResult({ "nInserted" : 1 })
````
#### 4)
#### a)
````
 > db.Hospital.find({Specialization:"Pediatric"})
````
#### b)
````
>
db.Hospital.find({Hname:"CCC","Doctor.Visit":"Tuesday"})
````
#### c)
````
>
db.Hospital.find({Specialization:{$not:{$size:1}},"Doctor.Dna
me":"XXX"})
````
#### d)
````
 > db.Hospital.find({"People.Rating":{ $gt: 3
},Hname:"AAA"})
````
**************************************************
#### slip 5
#### 2)&3)=>
````
>
db.post.insert({title:"online",url:"www.abc.com",tag:["food",
"travel"],pname:"mukesh",pdate:new Date("2019-03-
12"),like:89,user:[{name:"abhi",comment:"good",message:"
do best", cdate:new Date("2020-03-12"),like:1}]})
WriteResult({ "nInserted" : 1 })
>
db.post.insert({title:"wetpet",url:"www.wetpet.com",tag:["fo
od","travel",],pname:"Amit",pdate:new Date("2018-03-
12"),like:82,user:[{name:"abhi",comment:"good",message:d
obest",time:"4pm",like:1},{name:"mukesh",comment:"best",
message:"success", cdate:new Date("2008-11-12"),like:2}]})
WriteResult({ "nInserted" : 1 })
>
db.post.insert({title:"wetpet",url:"www.wetpet.com",tag:["fo
od","travel","magic"],pname:"abhijeet",pdate:new
Date("2017-03-
12"),like:182,user:[{name:"sagar",comment:"like",message:"
dobest",time:"4pm",like:1},{name:"mukesh",comment:"best"
,message:"success", cdate:new Date("2019-03-
12"),like:2}]})
WriteResult({ "nInserted" : 1 })
>
db.post.insert({title:"nonveg",url:"www.non.com",tag:["food
","travel","chiken"],pname:"Amit",pdate:new Date("2019-07-
12"),like:82,user:[{name:"manisha",comment:"good",messa
ge:"dobest",time:"4pm",like:0},{name:"manasi",comment:"b
est",message:"success", cdate:new Date("2018-03-
12"),like:0}]})
WriteResult({ "nInserted" : 1 })
````
#### 4)
#### a)
````
 >db.post.find({tag:"food"})
````
#### b)
````
 >db.post.find({pname:"Amit"})
````
#### c)
````
 > db.post.find({tag:"travel",pdate:{"$lte":new Date("2018-
03-11")},"user.name":"sagar","user.comment":"like"})
````
#### d)
````
 > db.post.find({$or:[{"user.cdate":{$lte:new Date("2019-
08-07")}},{"user.like":0}]})
````
**************************************************
#### slip6
#### 2)&3)=>
````
> db.turisum.insert({name:"veena
word",rate:9,package:[{pname:"shillong",cost:10000},{pnam
e:"gujart",cost:7000},{pname:"karnataka",cost:6000}]})
>
db.turisum.insert({name:"rohit",rate:7,package:[{pname:"shil
long",cost:10000},{pname:"rujan",cost:7000}]})
>
db.tour.insert({sourc:"john",destination:"shillong",toerisumN
ame:"veenaword",tourisumrate:8000,expense:20000,year:2
018,custome
r:[{cname:"mukesh",city:"pune"},{cname:"abhijeet
sangita",city:"baramati"},{cname:"manisha",city:"15no"},{cna
me:"manasi",city:"latur"}]})
>
db.tour.insert({sourc:"john",destination:"karnataka",toerisu
mName:"veenaword",tourisumrate:80090,expense:20900,y
ear:2017,custom
er:[{cname:"mukesh",city:"pune"},{cname:"abhijeet
sangita",city:"baramati"},{cname:"manisha",city:"15no"},{cna
me:"manasi",city:"latur"}]})
>
db.tour.insert({sourc:"john",destination:"rajasthan",toerisum
Name:"rohit",tourisumrate:6000,expense:30400,year:2019,
customer:[{cname:"mukesh",city:"pune"},{cname:"abhijeet
sangita",city:"baramati"},{cname:"manisha",city:"15no"},{cna
me:"manasi",city:"latur"}]})
>
db.tour.insert({sourc:"john",destination:"taj",toerisumName:
"rohit",tourisumrate:60090,expense:10400,year:2016,custo
mer:[{cname:"mukesh",city:"pune"},{cname:"abhijeet
sangita",city:"baramati"},{cname:"manisha",city:"15no"},{cna
me:"manasi",city:"latur"}]})
````
#### 4)
#### a)
````
 >db.turisum.find({name:"veena word"}).pretty()
````
#### b)
````
 >db.turisum.find({}).sort({"rate":-1}).limit(1)
````
#### c)
````
 >
db.tour.aggregate([{"$sort":{"year":1}},{"$limit":3},{$group:{
_id:null,"count":{"$sum":"$expense"}}}])
````
#### d)
````
 > db.tour.find({destination:"shillong"})
````
**************************************************
#### slip 7
#### 2)&3)=>
````
> db.scien.insert({fname:"mukesh",lname:"navse",BOD:new
Date("1952-04-
18"),DOD:"stillalive",field:["tcs","java","c","sql"],award:[{nam
e:"turing
machine",year:1976},{name:"robotic",year:1998},{name:"co
de talent",year:1995}]})
WriteResult({ "nInserted" : 1 })
> db.scien.insert({fname:"abhi",lname:"nalave",BOD:new
Date("1972-04-
18"),DOD:"stillalive",field:["tcs","java","sql"],award:[{name:"c
odemaster",year:1976},{name:"robot",year:1998},{name:"pu
zzletalent",year:1995}]})
WriteResult({ "nInserted" : 1 })
>
db.scien.insert({fname:"manisha",lname:"hipparkar",BOD:n
ew Date("1942-04-18"),DOD:new Date("2009-08-
06"),field:["tcs","java"],award:[{name:"topper",year:1976},{n
ame:"puraskar",year:1998},{name:"puzzletalent",year:1995}
]})
WriteResult({ "nInserted" : 1 })
````
#### 4)
#### a)
````
 > db.scien.find({ lname: { $regex: /n/ } })
````
#### b)
````
 > db.scien.find({BOD:{"$gt":new Date("1950-03-
11")},DOD:"still alive"})
````
#### c)
````
>db.scien.aggregate([{$group:{_id:{year:"$award.year",Nam
e
:"$award.name"}}}])
````
#### d)
````
 > db.scien.find({"award.name":"turing
machine","award.year":{$lt:1980},field:{$size:4}})
````
**************************************************
#### slip8
#### 2)&3)=>
````
>
db.item.insert({itemName:"planner",tag:["wash","food","veh
icle"],status:"A",height:5,width:9,instack:15,warehouse:[{loc
ation:"pune",quntity:36},{location:"mumbai",quntity:67}]})
WriteResult({ "nInserted" : 1 })
>
db.item.insert({itemName:"toycar",tag:["food","vehicle"],sta
tus:"D",height:5,width:9,instack:15,warehouse:[{location:"pu
ne",quntity:36},{location:"mumbai",quntity:67}]})
WriteResult({ "nInserted" : 1 })
> db.item.insert({itemName:"robotic
car",tag:["food","vehicle"],status:"A",height:9,width:9,instack
:5,warehouse:[{location:"pune",quntity:26},{location:"mumb
ai",quntity:17}]})
WriteResult({ "nInserted" : 1 })
>
db.item.insert({itemName:"bag",tag:["food","vehicle","schoo
l","travel"],status:"c",height:19,width:39,instack:75,warehou
se:[{location:"surat",quntity:26},{location:"lanavala",quntity:
17}]})
> WriteResult({ "nInserted" : 1 })
````
#### 4)
#### a)
````
 > db.item.find({status:"D","warehouse.quntity":{$gt:30}})
````
#### b)
````
> db.item.find({"tag":{$size:3}})
````
#### c)
````
 >
db.item.find({$or:[{status:"A"},{"warehouse.quntity":{$lt:30},
height:{$gt:10}}]})
````
#### d)
````
 > db.item.find({itemName:"planner",instack:{$lt:20}})
````
**************************************************
#### slip 9
#### 2)&3)=>
````
>
db.transaction.insert({itemName:"toy",customerName:"john
",paymentmode:"debitcard",payment:8000})
WriteResult({ "nInserted" : 1 })
>
db.transaction.insert({itemName:"car",customerName:"john
",paymentmode:"creditcard",payment:4000})
WriteResult({ "nInserted" : 1 })
>
db.transaction.insert({itemName:"bag",customerName:"muk
esh",paymentmode:"cash",payment:5000})
WriteResult({ "nInserted" : 1 })
>
db.transaction.insert({itemName:"airlineticket",customerNa
me:"rohit",paymentmode:"cash",payment:50090})
WriteResult({ "nInserted" : 1 })
>
db.transaction.insert({itemName:"mango",customerName:"a
bhijeet",paymentmode:"creditcard",payment:8000})
WriteResult({ "nInserted" : 1 })
>
db.transaction.insert({itemName:"bus",customerName:"man
asi",paymentmode:"debitcard",payment:7000})
WriteResult({ "nInserted" : 1 })
````
#### 4)
#### a)
````
 > db.transaction.find({customerName:"john"})
````
#### b)
````
 > db.transaction.find({paymentmode:"debitcard"})
````
#### c)
````
 >
db.transaction.aggregate([{$match:{"paymentmode":"creditc
ard"}},{$group:{_id:null,"count":{"$sum":"$payment"}}}])
````
#### d)
````
 >
db.transaction.aggregate([{$group:{_id:"$paymentmode","c
o
unt":{"$sum":"$payment"}}}])
````
**************************************************
#### slip10
#### 2)&3)=>
````
>
db.custome.insert({cname:"mukesh",modelname:"samsung
j6",amount:20000})
WriteResult({ "nInserted" : 1 })
>
db.custome.insert({cname:"abhijeet",modelname:"samsung
j6",amount:20060})
WriteResult({ "nInserted" : 1 })
> db.custome.insert({cname:"manasi",modelname:"iphone
7+",amount:30060})
WriteResult({ "nInserted" : 1 })
> db.custome.insert({cname:"manisha",modelname:"iphone
7+",amount:30070})
WriteResult({ "nInserted" : 1 })
> db.custome.insert({cname:"dipak",modelname:"iphone
7+",amount:30800})
WriteResult({ "nInserted" : 1 })
>
db.shopping.insert({brandname:"samsung",rate:6,model:[{m
name:"s40",ram:"3GB",rom:"32GB",rate:4},{mname:"j6",ram
:"4GB",rom:"32GB",rate:7},{mname:"j7",ram:"6GB",rom:"64
GB",rate:6}]})
WriteResult({ "nInserted" : 1 })
>
db.shopping.insert({brandname:"vivo",rate:8,model:[{mnam
e:"Y55",ram:"3GB",rom:"32GB",rate:6},{mname:"Ys5",ram:"
4
GB",rom:"32GB",rate:4},{mname:"YYY",ram:"6GB",rom:"64
G
B",rate:6}]})
WriteResult({ "nInserted" : 1 })
````
#### 4)

#### a)
````
>db.shopping.find({"model.ram":"3GB","model.rom":"32GB"})
````
#### b)
````
> db.custome.find({modelname:"samsung j6"})
````
#### c) 
````
> db.shopping.aggregate([{"$sort":{"rate":-
1}},{"$limit":1},{$group:{_id:"$brandname"}}])
````
#### d)
````
> db.custome.find().sort( { "cname": 1 } )
````
**************************************************
