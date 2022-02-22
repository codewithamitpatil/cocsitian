# cocsitian

# Debounce 

```
function debounce(fn, wait) {
    var timeout;
    return function () {
        var args = arguments;
        timeout && clearInterval(timeout);
        timeout = setTimeout(function () {
            timeout = null;
            fn.apply(null, args);
        }, wait);
    }
}

function print(){
 connsole.log('hello amit');
}

print = debounce(print,1000);

```

# Throtel

```
function throtel(fn, wait) {
    var timeout;
    return function () {
        var args = arguments;
        if (timeout) {
            return;
        }
        timeout = setTimeout(function () {
            timeout = null;
            fn.apply(null, args);
        }, wait);
    }
}


function print(){
 connsole.log('hello amit');
}

print = throtel(print,1000);

```
