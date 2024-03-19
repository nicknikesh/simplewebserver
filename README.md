# EX01 Developing a Simple Webserver
## Date: 19/02/2024

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
     <head>
         <Title>Top Software Companies Revenue</title>
     </head>
     <body>
     <table border="4" cellspacing="5" width="40" height="50"
       <caption>REVENUE</caption>
       <tr>
           <th>Rank</th>
           <th>Company name<\th>
           <th>Hourly Rates</th>
           <th>No of employees</th>
        </tr>
        <tr>
             <td>1</td>
             <td>Arateg</td>
             <td>$25-$49</td>
             <td>10-49</td>
        </tr>
        <tr>
             <td>2</td>
             <td>Codica</td>
             <td>$25-$49</td>
             <td>10-49</td>
        </tr>
        <tr>
             <td>3</td>
             <td>Webkul</td>
             <td>$25-$49</td>
             <td>200-500</td>
        </tr>
        <tr>
             <td>4</td>
             <td>uptech</td>
             <td>$50-$99</td>
             <td>50-249</td>
        </tr>
        <tr>
             <td>5</td>
             <td>Bilberrry</td>
             <td>$100-$149</td>
             <td>10-49</td>
        </tr>
        </table>
        </body>
        </html>
             




       


"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![alt text](<Screenshot 2024-03-19 132647.png>)


![alt text](<Screenshot 2024-03-19 132753.png>)


## RESULT:
The program for implementing simple webserver is executed successfully.
