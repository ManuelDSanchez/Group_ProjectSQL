# [Mist 4610 Group Project 1] 

## Team Members:

1. Manuel Sanchez [@manueldsanchez](https://www.github.com/manueldsanchez)
2. Stefan Mijatovic [@mijatovicstefan](https://www.github.com/mijatovicstefan)
3. Jake Lane [@jakeklane](https://www.github.com/jakeklane)
4. Jackson Lundmark [jlundmark9](https://www.github.com/jlundmark9)

## Problem Description:
The task that was given was to construct a relational database for a men’s and women’s soccer club based out of Athens, GA called “Georgia United FC”. The central entity of our database is Team, this being both the men’s and women’s team. The team is directly tied to facilities, matches, fans, finances, ect. which are the aspects that are connected to running our team. We worked to depict the database with the correct relationships, generating data for each entity, and then populating the database with the entities and corresponding attributes. With that data, we also planned to perform working queries that allow us to further increase our comprehension of the team and all of the subsequent operations.

## Explanation of data model:
Our data model is a representation of a soccer club called “Georgia United FC”. This club consists of a men’s and women’s team which is at the center of our database under the Team entity.  A team has a roster size, record, gender, and year. A team consists of many players and are connected by a one-to-many relationship. This is due to the fact that players can only reside in one team, respectively. Players have a first and last name, date of birth, position, nationality, contract length, and youth development. 
The facilities are separate for each team, for example the women’s have their own gym and the men’s have their own field. This makes it a one-to-many relationship as each one team has many facilities. Facilities are described by name, location, schedule, amenities, and capacity. In these facilities there’s only one place that record many injuries, and injuries consist of type, date, and date of return. 
Our team has many matches that each have a date, venue, opponent, score, and outcome. The matches entity is connected to the tournament entity with a one-to-many relationship as there is only one tournament taking place that consists of many matches in said tournament. This tournament contains the following information, name, venue, start and end date, and city. The tournament entity also contains a one-to-one recursive relationship due to the previous tournaments being recorded.
The team has people that are fans for both the men’s and women’s team so the relationship between these entities is a many-to-many relationship because a person can be a fan for both teams. The only information for the fans are their first and last names. There’s also fan feedback that connects to fans and teams as both have a one-to-many relationship to fan feedback. Fans are giving the feedback and the feedback pertains to the teams. Fan feedback has the following attributes, first name, last name, comment, and date.
The team is also composed of coaches who have a first name, last name, years of experience, position (head coach and assistant coach), record, and contract start and end. The coaches and players entities also share a many-to-many relationship as the players have multiple coaches and coaches train multiple players.
Finances are a one-to-many relationship with teams because we are under the assumption that both the men’s and women’s are under the same finances. In the finances we have transaction date, transaction type, amount, financial category, and payment method. 
Lastly, we have three separate entities that share a one-to-many relationship with finances as they are what is going into the finance account. This being tickets, merchandise, and sponsors. Tickets and Merchandise contain both price and amount sold. Sponsors have a name, contract start, contract finish, and sponsor amount. 

![Screenshot 2023-11-07 215008](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/b42eeff3-f28c-433e-987c-09d060b1fbc8)
