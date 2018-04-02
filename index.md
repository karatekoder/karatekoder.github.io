<!DOCTYPE html>
<html>
        <head>
            <!--meta viewport-->
            <meta charset="UTF-8" name="viewport" content="width=device-width, initial-scale=1.0">
            <link href="style.css" rel="stylesheet">
            <Title>Calculate with Java</Title>
            <script>
                var newNumber;
                newNumber = 0;
                var evensCount = 0;
                var even = 0;
                var evenSum = 0;
                var odd = 0;
                var oddsCount = 0;
                var oddSum = 0;
                var oddAverage = 0;
                var evenAverage = 0;
                    
                function Calculate() {
                    newNumber = parseInt(document.getElementById("enteredNumber").value);
                    if (isNaN(newNumber)){
                        alert("Please enter only numerical values");
                    }
                    else {
                        if ( newNumber != 0) {
                            if (newNumber % 2 == 0){
                                // even number - remainder is zero
                                even = newNumber;		
                                evensCount += 1;
                                evenSum += even;
                                evenAverage = evenSum/evensCount;
                                document.getElementById("evenNumSum").innerHTML = evenSum;
                                document.getElementById("evenNumAvg").innerHTML = evenAverage;
                            } 
                            else {
                                // odd number - remainder is 1
                                //alert ("Number " + number + " is odd");
                                odd = newNumber;
                                oddsCount += 1;
                                oddSum += odd;
                                oddAverage = oddSum/oddsCount;
                                document.getElementById("oddNumSum").innerHTML = oddSum;
                                document.getElementById("oddNumAvg").innerHTML = oddAverage;
                            }
                        }
                        else if (newNumber==0){
                            alert("Please only enter integers greater than 0");
                        }
                    
                    }
                }
        </script>
        </head>
        <header>
            <h1>Assignment 1</h1>
        </header>
        <body>
            <h2>Purpose</h2>
            <img src="calculator.jpg">
            <p>This page employs a number of dynamic HTML features to perform various calculations. When you, the user, enters any number and hits "Calculate", the page determines a 
                number of things.<br \>
                First it will determine whether the input is even a number or not, using the "isNaN" javascript feature. If the submission is indeed not a number, 
                then the window will alert you accordingly.<br \>
                Once the page has determined you have enterd a number, it will determine whether the number is 0. For this assignment, the user is must only enter nonzero numeric values. <br \> 
                As with the iNaN scenario, the window will alert you accordingly. <br\>
                Once the user's submission has passed these requirments, only then will the program begin to calculate.<br>
                This page is dynamic, meaning the values displayed changes as the user inputs more numbers.<br \>
                The specific calculations displayed are the sum and averages of the even and odd numbers entered.</p>
            <br \>
            Enter a number &nbsp; &nbsp;<input type="text" id="enteredNumber"> &nbsp; &nbsp;
            <input type="button" id="submitbn" onclick="Calculate();" value="Calculate">
            <br \><br \>
            The sum of the odd numbers you've entered is: <p id="oddNumSum"></p>
            The average of the odd numbers you've enterd is: <p id="oddNumAvg"></p>
            The sum of the even numbers you've enterd is: <p id="evenNumSum"></p>
            The average of the even numbers you've entered is: <p id="evenNumAvg"></p>
        </body>
        <footer>
            <p>Made by <i>Michael Kariuki</i> for PROG 1800 Assignment 1. Due February 13, 2018</p>
        </footer>
    </html>
