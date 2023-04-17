## Admin Has The Power Write-Up

### The first thing that came to my mind was to inspect the page to view the cookies of the webpage. 

### I found a cookie that has the name role and value support, so the first thing that came to my mind was to change its value to admin and see what I will get.

I viewed page source and found this commented code snippet:

```javascript
<!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->

<!--[if lt IE 9]>

<script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>

<script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>

<![endif]-->

<!-- TODO: remove this line , for maintenance purpose use this info (user:support password:x34245323)-->
```


We can see that the username is  "support" and the password is "x34245323".

After entering these credentials we get the following message: 

> Hi support
> Your privilege is support , may be you need better privilages !!

I used the cookie I found before to change its value to admin and see what I will get.

That opened a new page with the falg in it 

>  Hi admin
> Admin Secret flag :  ######################

