# Loading
IN HTML &amp; CSS
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="l.css">
</head>
<body>
    <div class="center">
        <div class="ring"></div>
        <span>Loading...</span>
    </div>
</body>
</html>

<!--CSS FILE-->
body{
    margin: 0;
    padding: 0;
    font-family: montserrat;
    background: black;
}
.center{
    display: flex;
    text-align: center;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}
.ring{
    position: absolute;
    width: 200px;
    height: 200px;
    border-radius: 50%;
    animation: ring 2s linear infinite;
}
@keyframes ring{
    0%{
        transform: rotate(0deg);
        box-shadow: 1px 5px 2px red;
    }
    50%{
        transform: rotate(180deg);
        box-shadow: 1px 5px 2px yellow;
    }
    100%{
        transform: rotate(360deg);
        box-shadow: 1px 5px 2px rgb(58, 19, 198);
    }
}
.ring::before{
    position: absolute;
    content: ' ';
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    border-radius: 50%;
    box-shadow: 0 0 5px rgba(255, 255, 255, 0.3);
}
span{
    color: antiquewhite;
    font-size: 20px;
    text-transform: uppercase;
    letter-spacing: 1px;
    line-height: 200px;
    animation: text 3s ease-in-out infinite;
}
@keyframes text{
    50%{
        color: black;
    }
}
