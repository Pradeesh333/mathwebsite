# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :

```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">

  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Volume Calculator</title>
</head>

<body>

  <div class="formelement">
    <h1><small>Volume Calculator For Cylinder And Cone</small></h1>
  </div>
  <div class="container">
    <div class="content">
      <h1>Volume Of Cylinder</h1>
      <form>
        <div class=formelement>
          <lable for="aedit">Height:</lable>
          <input id="aedit" placeholder="" />
          <label><small>
              Meters
            </small></label>
        </div><br>
        <div class=formelement>
          <lable for="bedit">Radius:</lable>
          <input id="bedit" placeholder="" />
          <label><small>
              Meters
            </small></label>
        </div><br>
        <div class=formelement>
          <lable for="cedit">Volume:</lable>
          <input type="number" min="0" value="0" step="any" id="cedit" placeholder="0" readonly="0" /><label><small>
              Meters³</small></label>
        </div><br><br>
        <div class=formelement>
          <input type="button" class="button" value="CALCULATE" id="calbutton1" />
          <input type="Reset" class="button" value="RESET">
        </div>
        <center>
          <p id="stats1"></p>
        </center>
        <br>
        <div class=formula>
          Formula is
          Volume V = π X Radius² X Height
        </div><br>
      </form>
    </div>

    <div class="content2">
      <h1>Volume of Cone</h1>
      <form>
        <div class="formelement">
          <lable for="radiusedit">Radius:</lable>
          <input id="radiusedit" placeholder="" />
          <label><small>
              Meters
            </small></label>
        </div><br>
        <div class="formelement">
          <lable for="heightedit">Height:</lable>
          <input id="heightedit" placeholder="" />
          <label><small>
              Meters
            </small></label>
        </div><br>
        <div class="formelement">
          <lable for="volumeedit">Volume:</lable>
          <input type="number" min="0" value="0" name="avol" step="any" id="volumeedit" placeholder="0"
            readonly="0" /><label><small> Meters³</small></label>
        </div><br><br>
        <div class="formelement">
          <input type="button" class="button" value="CALCULATE" id="calbutton2" />
          <input type="Reset" class="button" value="RESET">
        </div><br>
        <center>
          <p id="stats2"></p>
        </center>
        <div class="formula">
          Formula is:
          Volume V = π X Radius² X Height / 3
        </div>

        <br>
      </form>

    </div>
  </div>
  <div class="fbox">
    <div class="footer">
      <center>
        <p><br>
          Made by Pradeesh S
        </p>
      </center>
    </div>
  </div>
</body>
<script type="text/javascript">
  var button;
  button = document.querySelector("#calbutton1");
  button.addEventListener("click", function () {
    var atext, btext, ctext;
    var aval, bval, cval;
    let text1
    atext = document.querySelector("#aedit");
    btext = document.querySelector("#bedit");
    ctext = document.querySelector("#cedit");

    if (Number(atext.value) && Number(btext.value)) {
      aval = parseInt(atext.value);
      bval = parseInt(btext.value);
      text1 = "The Answer Is Generated Successfully!!!";

    }
    else {
      window.alert("The Number You Entered Is `Invalid Format`. Click Reset And Try Again!!!");
      text1 = "Error or Invalid Format!!!";
    }

    cval = 3.14 * aval * aval * bval;
    ctext.value = "" + cval;

    document.getElementById("stats1").innerHTML = text1;

  });
</script>
<script type="text/javascript">
  var button;
  button = document.querySelector("#calbutton2");
  button.addEventListener("click", function () {

    var radiustext, heighttext, volumetext;
    var aval, bval, cval;
    var text2
    radiustext = document.querySelector("#radiusedit");
    heighttext = document.querySelector("#heightedit");
    volumetext = document.querySelector("#volumeedit");

    if (Number(radiustext.value) && Number(heighttext.value)) {
      aval = parseInt(radiustext.value);
      bval = parseInt(heighttext.value);
      text2 = "The Answer Is Generated Successfully!!!";
    }
    else {
      window.alert("The Number You Entered Is `Invalid Format`. Click Reset And Try Again!!!");
      text2 = "Error or Invalid Format!!!";
    }

    cval = 3.14 * aval * aval * bval / 3;
    volumetext.value = "" + cval;

    document.getElementById("stats2").innerHTML = text2;

  });

</script>

<style>

  .container {
    grid-gap: 50px;
    width: 1080px;
    margin-left: auto;
    margin-right: auto;
  }

  .content {
    display: block;
    width: 100%;
    background-color: rgb(214, 163, 255);
    min-height: 500px;
    margin-top: 50px;
    margin-bottom: 50px;
    box-shadow: inset 0 0 15px rgb(111, 0, 255);
    backdrop-filter: blur(9px);
    border-radius: 10px;
    border: 5px solid rgb(220, 166, 255);
  }

  .content2 {
    display: block;
    width: 100%;
    background-color: rgb(214, 163, 255);
    min-height: 500px;
    margin-top: 50px;
    margin-bottom: 50px;
    box-shadow: inset 0 0 15px rgb(111, 0, 255);
    backdrop-filter: blur(9px);
    border-radius: 10px;
    border: 5px solid rgb(220, 166, 255);
  }

  .fbox {
    display: block;
    width: 100%;
    background-color: rgb(255, 255, 255);
    min-height: 100px;
    margin-top: 0px;
    margin-bottom: 0px;
    box-shadow: inset 0 0 15px rgb(140, 0, 255);
    backdrop-filter: blur(9px);
    border-radius: 10px;
    border: 5px solid rgb(98, 0, 255);
  }

  .button {
    background-color: rgb(255, 177, 251);
    border: 1px solid rgb(248, 237, 255);
    border-radius: 25px;
    color: rgb(76, 0, 255);
    padding: 15px 32px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
  }

  * {
    box-sizing: border-box;
    font-family: Century Gothic, sans-serif;
  }

  h1 {
    text-align: center;
    padding-top: 50px;
    color: rgb(128, 60, 255);
  }

  .formelement {
    text-align: center;
    font-size: x-large;
    margin-top: 5px;
    margin-bottom: 5px;

  }

  .formula {
    text-align: center;
    font-size: large;
    margin-top: 5px;
    margin-bottom: 5px;
  }

  .footer p {
    margin: 0;
    line-height: 26px;
    font-size: 35px;
    color: #8400ff;
  }

</style>
</html>
```

## OUTPUT:

![](output1.png)
![](output2.png)

## Result:

Thus a website is designed to perform mathematical calculations in the client side.
