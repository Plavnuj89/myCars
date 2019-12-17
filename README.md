function Transport(name,date,color,fromTo) {
    this.name = name;
    this.date = date;
    this.color = color;
    this.my =true;
    this.howManyYears = fromTo
}




var day = new Date().getFullYear();
var tavria = new Transport("Таврия", 2004,"красного",7);
var velo = new Transport("Аист", 1986,"зеленого", day - 1997);
var peugeot = new Transport("Пежо", 1997, "Белого",1);
var opel = new Transport("Опель",2007,"Синего",day-2019);
var tr  =[
    ["первым",velo.name,velo.color,velo.howManyYears],
    ["вторым",tavria.name,tavria.color,tavria.howManyYears],
    ["третьим",peugeot.name,peugeot.color,peugeot.howManyYears],
    ["четвертым",opel.name,opel.color,opel.howManyYears]
];
// console.log(velo);
// console.log(tavria);
// console.log(peugeot);
// console.log(opel);
console.log("Транспорт, которым я пользовался...")
tr.forEach(function (item) {
    var god = "лет"
if (item[3]==1||item[3]==21) {
    var god="год"
}
else if (item[3]>=2&&item[3]<5){
    var god = "года"

}else if (item[3]>=22) {
    var god = "года"

}
    console.log( `Моим ${item[0]} видом транспорта - был ${item[1]} он был ${item[2]} цвета, и я им пользовался  ${item[3]} ${god}`
    );
});
