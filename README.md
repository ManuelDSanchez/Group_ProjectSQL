# Mist 4610 Group Project 1

## Team Members:

1. Manuel Sanchez [@manueldsanchez](https://www.github.com/manueldsanchez)
2. Stefan Mijatovic [@mijatovicstefan](https://www.github.com/mijatovicstefan)
3. Jake Lane [@jakeklane](https://www.github.com/jakeklane)
4. Jackson Lundmark [jlundmark9](https://www.github.com/jlundmark9)

## Problem Description:
The task at hand was to construct a relational database for a men’s and women’s soccer club based out of Athens, GA called “Georgia United FC”. The central entity of our database is Team, this being both the men’s and women’s teams. The teams are directly tied to facilities, matches, fans, finances, etc. which are the aspects that are connected to running our team. We worked to depict the database with the correct relationships, generating data for each entity, and then populating the database with the entities and corresponding attributes. With that data, we also planned to perform working queries that allow us to further increase our comprehension of the team and all of the subsequent operations.

## Data Model:
Explanation of our Data model:
Our data model is a representation of a soccer club called “Georgia United FC”. This club consists of a men’s and women’s team which is at the center of our database under the Team entity.  A team has a roster size, record, gender, and year. A team consists of many players and are connected by a one-to-many relationship. This is due to the fact that players can only reside in one team, respectively. Players have a first and last name, date of birth, position, nationality, contract length, and youth development. 
The facilities are separate for each team, for example the women’s have their own gym and the men’s have their own field. This makes it a one-to-many relationship as each one team has many facilities. Facilities are described by name, location, schedule, amenities, and capacity. In these facilities there’s only one place that record many injuries, and injuries consist of type, date, and date of return. 
Our team has many matches that each have a date, venue, opponent, score, and outcome. The matches entity is connected to the tournament entity with a one-to-many relationship as there is only one tournament taking place that consists of many matches in said tournament. This tournament contains the following information, name, venue, start and end date, and city. The tournament entity also contains a one-to-one recursive relationship due to the previous tournaments being recorded.
The team has people that are fans for both the men’s and women’s team so the relationship between these entities is a many-to-many relationship because a person can be a fan for both teams. The only information for the fans are their first and last names. There’s also fan feedback that connects to fans and teams as both have a one-to-many relationship to fan feedback. Fans are giving the feedback and the feedback pertains to the teams. Fan feedback has the following attributes, first name, last name, comment, and date.
The team is also composed of coaches who have a first name, last name, years of experience, position (head coach and assistant coach), record, and contract start and end. The coaches and players entities also share a many-to-many relationship as the players have multiple coaches and coaches train multiple players.
Finances are a one-to-many relationship with teams because we are under the assumption that both the men’s and women’s are under the same finances. In the finances we have transaction date, transaction type, amount, financial category, and payment method. 
Lastly, we have three separate entities that share a one-to-many relationship with finances as they are what is going into the finance account. This being tickets, merchandise, and sponsors. Tickets and Merchandise contain both price and amount sold. Sponsors have a name, contract start, contract finish, and sponsor amount. 

![Screenshot 2023-11-07 215008](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/b42eeff3-f28c-433e-987c-09d060b1fbc8)

## Data Dictionary

![image](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/55907df4-1114-411d-9fcb-935dceadf9b4)

![Screenshot 2023-11-07 221608](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/bbe06d0a-b244-410e-a509-e57c9b5d836f)

![Screenshot 2023-11-07 221615](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/5d60f00c-3f42-4125-ab04-b78fed84c4a1)

![Screenshot 2023-11-07 221629](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/3f18db9b-ffae-4e9d-9c0b-05a1bed8fbb0)

![Screenshot 2023-11-07 221639](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/d4804d64-dbf7-401c-addb-0f65a96109e0)

![Screenshot 2023-11-07 221650](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/24d812a6-f907-4c74-aca5-593a85ed3a75)

![Screenshot 2023-11-07 221658](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/6dc0dbc4-714f-4e4f-b65b-5801ac4893fa)

![Screenshot 2023-11-07 221715](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/653761e0-846e-4aa2-8686-cc487e0ceb25)

![Screenshot 2023-11-07 221724](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/4efc4794-f8b6-4ed8-addd-d25193f6721f)

![Screenshot 2023-11-07 221745](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/7ed907de-7a2e-4dcf-8b57-f949ea31feb0)

![Screenshot 2023-11-07 221750](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/01cd4185-635a-434a-a41c-7bad87fb8756)

![Screenshot 2023-11-07 221758](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/adce6419-bd52-4085-8294-cd3f178eecf4)

![Screenshot 2023-11-07 221809](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/5da3330c-aade-4fd0-a728-8af97c479c0c)

![Screenshot 2023-11-07 221814](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/2e94652e-4f86-48fa-a3df-d6d3c95e3b36)

![Screenshot 2023-11-07 221820](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/9e6b27b4-1e2a-4a9b-be65-140c25367484)

![Screenshot 2023-11-07 221834](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148247767/59001842-28f6-4903-bb58-47400cf63e9a)


## Queries:
![Screenshot 2023-11-07 221718](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/f4b5d809-cead-42f8-a307-a59ec82e5400)

![Screenshot 2023-11-07 222007](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/869d03dc-9dc7-487e-a690-0ba6eada0949)
![Screenshot 2023-11-07 222016](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/87036ae3-a92a-44cf-98a0-f931255a1d86)
![Screenshot 2023-11-07 222034](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/eb4c303a-b15b-4b62-b8fa-fad89d2b6022)
![Screenshot 2023-11-07 222041](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/97916fe3-23f3-47ff-b2aa-27f4137fc69b)
![Screenshot 2023-11-07 222052](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/e8b95c4d-f674-443e-ad39-7808afb3dddb)
![Screenshot 2023-11-07 222104](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/f982d4a1-3320-4acd-a8ef-df62f5673825)
![Screenshot 2023-11-07 222120](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/e2b5cd9f-ddd6-42fd-a5a0-4b9132d6d34f)
![Screenshot 2023-11-07 222128](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/9c24be6c-e474-4620-874a-04c176707005)
![Screenshot 2023-11-07 222137](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/4eb20ea8-e511-45f0-9b06-313661e57838)
![Screenshot 2023-11-07 222146](https://github.com/ManuelDSanchez/Group_ProjectSQL/assets/148248019/f77ca398-85ce-4cab-8b32-cfb84891b690)
