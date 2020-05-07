# Google Hash Code 2020

This code, fully done by my teammate and me during Google's 2020 Hash Code competition, tries to solve this year's problem.

The main objective was to obtain the highest score by scanning different books that were distributed over different libraries in a limited number of days. Copies of the same book could be available in more than one library. Each book was assigned a score, and points could only obtained once per book (i.e. scanning two copies of the same books will only award points once). Moreover, each library had a certain “signup” time (start-up/initiation time) and a different throughput (number of books that can be scanned per day). Only one library can be performing the signup process at each time instance, while scanning of books can be done in parallel.

## Our heuristic solution

We used a greedy approach. We firstly sorted the libraries based on the signup time and the best possible score as a result of scanning the books of the libraries. We also controlled that the same book wasn't added more than one time. 

## A possible improovement
What we did was to iterate through each library to add its books after having sorted the libraries based on the signup time. So a possible improovement would be sorting the libraries after every iteration (of a library) because the books inside the other libraries may have changed (i.e, if a book is repeated in multiple libraries)
