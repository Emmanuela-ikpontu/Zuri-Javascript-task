function convertFahrToCelsius (f) {
  let c = (f - 32) * 5/9;
  let fahr = Object.prototype.toString.call(f);
  if (fahr ==="[object Number]" || (fahr === "[object String]" && !isNaN(f))){
  //Return your output here
     return  c.toFixed(4);
  }
  else{
       // put error code here
       let paramtype = fahr.split(" ");
       paramtype[1] = paramtype[1]. substring(0, paramtype[1]. length-1);
       return `${JSON.stringify(f)} is not a valid number but a/an ${paramtype[1]}`;
  }
}

function checkYuGiOh(n) {
   let result =[];
    if(isNaN(n)) {
    return `invalid parameter: "${n}"`;
    }
    for (let i = 0; i <= n; i++) {
    let localvar=[];
    if (i % 2  == 0) {
     localvar.push("yu");
    }
    if (i % 3  == 0) {
     localvar.push("gi");
    }
    if (i % 5  == 0) {
     localvar.push("oh");
    }
    if (localvar.length > 0) {
      result.push(localvar.join("-"));
    }
    else {
      result.push(i);
    }
    }
      return result;
}
