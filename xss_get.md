# How to protect XSS_GET from bWAPP (easy level)

## Member group
* MR.ANGKARN  PUMMARIN
* MR.RAKSAPON  LEELACHAT
* MR.TANAPAD  ONSRI

## Test Vulnerability XSS
### Input <script>alert(1);</script> 
  ![Kahoot](xss_get03.png)
  
## Oh!!! 
### Alert
  ![Kahoot](xss_get04.png)

## Oh WOW!!!  
### bWAPP XSS_GET
  ![Kahoot](xss_get00.png)

## Scan with RIPS 
### Focus Cross-Site Scipting Topic
  ![Kahoot](xss_get01.png)
  
## Get Help RIPS
### related securing functions then use it :)
  ![Kahoot](xss_get02.png)


## let's fix it

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
 
## fix is correct  
### Complete
  ![Kahoot](xss_get04.1.png)

## Force will be with you  
### Complete
  ![Kahoot](xss_get05.png)
