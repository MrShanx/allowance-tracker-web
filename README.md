
<!DOCTYPE html>
<!--
To change this license header, choose License Headers in Project Properties.
To change this template file, choose Tools | Templates
and open the template in the editor.
-->
<html>
    <head>
        <title>Allowance</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        
        <!-- style sheet goes here -->
        <link rel="stylesheet" type="text/css" href="../sheets/mainpage_stylesheet.css">
        
        <!-- scripts here -->
        <script src="../scripts/mainpage_script.js">
        </script>
    </head>
    <body onLoad="funcInitPage()">
        <div id="page">
            <div id="top">
                <h1>Allowance remaining:</h1>
                    <form onsubmit="return false">
                        <input type="text" id="allowance_out" value="Add Allowance" readonly>                         
                    </form>
            </div>
            <div id="bottom">
                <form name="bottom_form" id="bottom_form" onsubmit="return false">
                Expense:
                    <input type="number" id="expense_in" value="" step="0.25" min="0.00" max="99999"
                           onkeydown="if(event.keyCode === 13) {
                                            document.getElementById('subtract_button').click();
                                    }"
                                     autofocus>
                <br/>
                    <textarea name="expense_log" id="expense_log" form="bottom_form" readonly></textarea><br/>                                   
                    <input type="button" id="add_button" onClick="add()" value="Add Allowance">
                    <input type="button" id="subtract_button" onClick="subtract()" value="Add Expense">                
            <br/> 
                <input type="button" id="res_button" onClick="res()" value="Reset">
                </form>                
            </div>
            <div id="footer">
                <p>Copyright &copy; 
                    <script type="text/javascript">
                        var d = new Date();
                        document.write(d.getFullYear());
                    </script>
                    <a href="https://www.linkedin.com/in/emmanueltalan" target="_blank">[emmanuel talan]</a></p>
            </div>
        </div>
    </body>
</html>
