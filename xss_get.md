# How to protect XSS_GET from bWAPP (easy level)

## Member group
* MR.ANGKARN  PUMMARIN
* MR.RAKSAPON  LEELACHAT
* MR.TANAPAD  ONSRI

### Scan with RIPS and Focus Cross-Site Scipting Topic
  ![Kahoot](xss_get01.png)

## let's for fix it

### Original Code

    <?php

    if(isset($_GET["firstname"]) && isset($_GET["lastname"]))
    {   

       * $firstname = $_GET["firstname"];
       * $lastname = $_GET["lastname"];
        

        if($firstname == "" or $lastname == "")
        {

            echo "<font color=\"red\">Please enter both fields...</font>";       

        }

        else            
        { 

            echo "Welcome " . xss($firstname) . " " . xss($lastname);   

        }

    }

    ?>
    
    
    
### Secure Coding
    
     <?php

    if(isset($_GET["firstname"]) && isset($_GET["lastname"]))
    {   

        //$firstname = $_GET["firstname"];
        //$lastname = $_GET["lastname"];
        
      * $firstname = htmlspecialchars($_GET["firstname"]);
      * $lastname = htmlspecialchars($_GET["lastname"]);

        if($firstname == "" or $lastname == "")
        {

            echo "<font color=\"red\">Please enter both fields...</font>";       

        }

        else            
        { 

            echo "Welcome " . xss($firstname) . " " . xss($lastname);   

        }

    }

    ?>
