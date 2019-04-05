Add your answers to the Algorithms exercises here.
exercise 1
I
this code has a complexity of O(n), because n^2 will have to added to itself n times to equal n^3.
The code will add n^2 to 0 then procede to add n^2 to the accumulated number untill the value is not less than n^3.

II
I'm not for sure what the complexity is, but I do know that as n grows so does the number of times that each loop must run. my brain isnt working enough to figure out the rate of growth though....

III
I think this is O(n), because I think the function will run recursively n times and will look something
like this bunnyEars(n-1) + bunnyEars(n-2) + bunnyEars(n-3) ......+ bunnyEars(n-n). 

exercise 2
The first solution that comes to mind would be. first drop the egg from the top floor if it dosent break then f must be equal to or greater than n so n would be our best guess. next if the egg breaks from the top move to the middle and drop the egg. if the egg breaks go to the middle of the last tested floor and the ground floor. if the egg stays whole move to the middle of the last droped floor and the top floor. repeat these steps till you find the magic floor f replacing the bottom and top floors with the closest tested floors up or down .