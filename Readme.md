*Power plant coding challenge* 

***
* Context

The goal of the project is to calculate how much power each of a multitude of different powerplants need to produce 
(a.k.a. the production-plan) when the load is given and taking into account the cost of the underlying energy sources 
(gas, kerosine) and the Pmin and Pmax of each powerplant.

The final result should appear like follow : 

{

    "name": "name of the power plant",
    "p": "power needed to acheived the load"
}

I suggest to use Postman application to use the API :

***

*REST API* 

* GET

After launching the API, go to the Postman application and copy past the url given in the terminal. Make sure that the 
methode selected in Postman is GET and once is it done click on SEND.
You should see the following message should appeared in the terminal "powerplant-coding-challenge"

By adding the endpoint /powerplants to the url you will be redirected to new page 
showing the initial payload (default payload1 - you can select another payload by directly entering its name at the 
appropriated location in the code)

* POST

This method is used to create a new power plant. To do so,  
you have to go to the endpoint /powerplants. Select the method POST in the Postman application. Once it is done go to 
the Header and under the item Key select "Content-type" and under the item value select "Application/json".
Then go to the body and select body. There you can create the new power plant. Following this structure :

    {   
        "name":"name of the power plant",
        "type": "type of the power plant",
        "efficiency": int,
        "pmin": int,
        "pmax": int
    }

Once the new power plant is created, you can click on SEND. You will see in the terminal that your new power plant has 
been added to the list of power plant.

After doing the creation and the adding of the new power plant. You can see the power generate by each power plant to 
achieve the load by going to the endpoint /productionplant.

    