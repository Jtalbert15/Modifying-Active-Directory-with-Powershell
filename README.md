# Modifying-Active-Directory-with-Powershell
In this lab we will modify active directory via powershell

Creating a user in Active Directory can also be done in A CLI 

To do this you can type New-ADUser

New specifies that we are creating something new

ADuser tells powershell that we are dealing with an Active Directory User

Keep in mind you can tab complete. Once you have typed New-ADUser hit enter

<img width="839" alt="Screenshot 2024-06-01 at 12 33 37 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/9fa0eecf-f8f4-44ba-a7f5-2832cb663543">

Now powershell will allow us to fill out the name of our user

<img width="343" alt="Screenshot 2024-06-01 at 12 36 25 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/372644f2-fabf-4fa9-aac9-d1c4c2e5f7d3">

Now we can check Active Directory to see if our newly created user is there

<img width="408" alt="Screenshot 2024-06-01 at 12 38 50 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/cd6b0d9e-efa1-44b6-b528-bf81eacc7907">

We can see that we did create our new user but there is hardly any information

Lets create a new user in powershell but this time we will add more information 

To do this we can use parameters. New-ADUser has many parameters but we will only use a few

To use a parameter after our New-ADUser we can use the - key

<img width="835" alt="Screenshot 2024-06-01 at 12 59 48 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/656a821b-e30b-4f17-a33f-e913f8134f3b">

Up above you can see we have created a user with the name Aaron a city of Orlando amongst other things

<img width="409" alt="Screenshot 2024-06-01 at 1 02 56 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/7865fb5c-42cc-44f2-8db7-52236d0d63e0">

You can see our user was created and the information we provided powershell was applied to the user

There are many more parameters we could have used but those were just a few

Now let's create an Organizational Unit in Active Directory

To do this we can type New-ADOrganizationalUnit

<img width="433" alt="Screenshot 2024-06-01 at 2 07 26 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/b29c3690-a263-4129-bd21-4e974202795b">

Just like before we can now provide a name for our organizational unit

<img width="749" alt="Screenshot 2024-06-01 at 2 08 38 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/f9c1994e-442b-4229-b3b9-5a8e03d108b1">

Now that we can see our IT OU lets create another OU within to store our IT users

To do this we can use the path parameter to specify where we want to create the new OU

<img width="666" alt="Screenshot 2024-06-01 at 2 58 09 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/c86bdab6-aa52-4390-94d3-0fd7f4040dd8">

To declare the path we need to go to our Active Directory and look at its file structure

So in this case the first part we see ou=it, this specifies that we are placing this OU in the IT organizational unit

Then above that in our case we have the domain

The domain is represented by DC and we need to split it up into two pieces 

<img width="751" alt="Screenshot 2024-06-01 at 3 06 05 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/5baeda09-398c-4372-bf0a-de32f8280d4a">

I've created a user in this folder we have just created

We can find out more information about this user using Get-ADUser

<img width="832" alt="Screenshot 2024-06-01 at 3 42 37 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/77c90ac0-ab08-4ec2-914e-08e4e9ba30f2">

identity specifies who we are searching for and properties set to * gets all the properties of this user

<img width="835" alt="Screenshot 2024-06-01 at 3 44 09 PM" src="https://github.com/Jtalbert15/Modifying-Active-Directory-with-Powershell/assets/66844406/edef161d-e4ca-40b6-b8c8-e50a67a994da">
