/*1)---------
IMPLEMENTAR UNA FUNCIÓN QUE TOME 2 NUMEROS COMO ARGUMENTOS (x y z) EN EL CUAL
SI x ES MENOR QUE z, x DIVIDE A z, CASO CONTRARIO SE MULTIPLICAN. RETORNAR
EL RESULTADO*/


const funcionDivMul=(x,z) => {
    if(x<z){
        var div = z/x;
        resultado = div;
    } else {
        var multi = x*z;
        resultado = multi;
    }
    return resultado;
}
console.log(funcionDivMul(10,5))



/* 2)---------
IMPLEMENTAR UNA FUNCIÓN QUE TOME UN VALOR COMO ARGUMENTO Y RETORNE DE QUE TIPO
ES (SI ES STRING, NUMBER, BOOLEAN, ETC) */

const funcionValores=(any) => {
    return typeof(any)
}
console.log(funcionValores("Lucas"))







/* 3)---------
IMPLEMENTAR UNA FUNCIÓN QUE TOME 6 VALORES (a,b,c,d,e,f) COMO ARGUMENTOS
- a y b SE SUMAN
- EL RESULTADO DE LA SUMA SE RESTA CON c
- LUEGO SE MULTIPLICA POR d Y SE DIVIDE POR e
- FINALMENTE SE HACE LA POTENCIA CON EL EXPONENTE f.
- SE RETORNA EL RESULTADO
- TIP: RECORDAR EL ORDEN */

const funcionSeisValores=(a,b,c,d,e,f) =>{
    let suma = a+b;
    let resta = c-suma;
    let multiDiv = (d*resta)/e;
    return multiDiv^f;
}

console.log(funcionSeisValores(2,2,2,2,2,2))



/* 4)---------
IMPLEMENTAR UNA FUNCIÓN QUE TOME UN ARRAY COMO ARGUMENTO Y SE EXTRAIGA LOS
ULTIMOS 3 ELEMENTOS. RETORNAR EL RESULTADO COMO UN NUEVO ARRAY. */
const frutas = ["banana", "manzana", "pera", "uva"]
const funcionArreglo=(array) => {    
    return [array[array.length-3], array[array.length-2], array[array.length-1]]
}
console.log(funcionArreglo(frutas))




/* 5)---------
IMPLEMENTAR UNA FUNCIÓN QUE TOME UN ARRAY COMO ARGUMENTO, ORDENAR ALFABÉTICAMENTE
Y/O DE MAYOR A MENOR Y RETORNAR EL RESULTADO */
const ordenar = [3,2,1,4,6, "b", "a", "c"]

const funcionOrdenar=(array) =>{
    array.sort();
    return array
}
console.log(funcionOrdenar(ordenar))



/* 6)---------
IMPLEMENTAR UNA FUNCIÓN QUE RECIBA COMO ARGUMENTO UN ARRAY (a) Y UN VALOR(b).
LA FUNCION DEBE REMOVER TODOS LOS ELEMENTOS DEL ARRAY IGUALES AL VALOR(b).
RETORNAR EL ARRAY FILTRADO */

const numeros = [1, 2, 3, 4, 5, 6, 6]

const funcionBorrarb=(array, b) =>{
    const funcionValores=(valores) => {
        return valores != b
    }
    const filtrado = array.filter(funcionValores)
    return filtrado
}
console.log(funcionBorrarb(numeros, 6))



/* 7)---------
IMPLEMENTAR UNA FUNCIÓN QUE RECIBA UN ARRAY DE NUMEROS COMO ARGUMENTO Y QUE
RETORNE LA SUMA DE LOS ELEMENTOS DEL ARRAY. IDEM A ESTE APARTADO CREAR OTRA
FUNCIÓN QUE RETORNE EL PROMEDIO DE LOS ELEMENTOS DEL ARRAY. */

const array1 = [1,2,3,4,5]

const funcionSuma=(array) => {
    let suma = 0;
    for (let i = 0; i<array.length; i++){
        suma += array[i];
    }
    return suma
}
const funcionPromedio=(array) => {
    let suma = 0;
    for (let i = 0; i<array.length; i++){
        suma += array[i];
    }
    return suma/array.length
}
console.log(funcionSuma(array1))
console.log(funcionPromedio(array1))

  


/* 8)---------
IMPLEMENTAR UNA FUNCIÓN QUE TOME: OBJETO CON 2 O 3 PROPIEDADES Y UN STRING
COMO ARGUMENTOS. DEBE RETORNAR EL VALOR DE LA PROPIEDAD CUYA KEY SEA IGUAL
AL VALOR DEL STRING DEL ARGUMENTO */

const objeto1 = {nombre: "auto", marca: "ford", color: "azul"}
const funcionKey=(object, key)=>{
    for(let argumento in object){
        if(argumento===key){
            return object[argumento]
        }
    }
}
console.log(funcionKey(objeto1, "marca"))



/* 9)---------
IMPLEMENTAR UNA FUNCIÓN QUE RECIBA UN OBJETO COMO ARGUMENTO Y RETORNAR
LA SUMA DE TODOS SUS VALORES. */

const valores = {valor1:20, valor2:40, valor3:50}

const funcionSumaObjeto=(object)=>{
    let suma=0;
    for (valor in object){
        suma+=object[valor];
    }
    return suma;
}
console.log(funcionSumaObjeto(valores))