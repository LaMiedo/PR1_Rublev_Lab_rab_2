# PR1_Rublev_Lab_rab_2
<!DOCTYPE html>
<html>
<body>
<input id="A" type="text" placeholder="a" value="1"><br>
<input id="H" type="text" placeholder="h" value="2"><br>
<input id="N" type="text" placeholder="n" value="3"><br>
<div id="result"></div>    
<script>
function f (x) {
     return (x * x + 1) * Math.pow(Math.cos(x), 2);
}

function F(a, h, n) {
    var res = f(a) + f(a + h * n);
    
    for(var i = 1; i < n; i++)
        res += 2 * f(a + h * i);
    
    return res;
}

function updateResult () {
    result.innerHTML = F(A.value, H.value, N.value);
}

$('input').keyup(updateResult);

updateResult();
</script>

</body>
</html>
