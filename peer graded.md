ANSWER-1:
1) Primary keys are userID and sessionID. There are another foreign key, missionID that point on the mission table.
2) Maybe Score (int) column should be added.
3) sessionID is long, because it grows very fast. MissionID int should be enough because there are limited missions. For isHit there are two options: ENUM with yes or no allowed input or simply string.

ANSWER-2:
1. find communities of users (teams) and count the number of sessions.
2. Group text messages based on users and two groups: based on edge type "leaves" and "join"+"starts"
3. create a document vector model and compute TF-IDF foreach text message sended within a specific time period.
4. Group nodes with edge type "write" by userID and sessionID  and count them. 
5. Group nodes with edge types "joins" or "starts" by userID and count them. 

ANSWER-3:
I should extend the flamingo properties because the game grows over time. New flamingos will be released in the future for free or paid and it should be enough difference and properties between each flamingo. This is useful for user engagement over time and user ranking.

Flamingo Properties:

- flamingoName (string) ex. "Real Flaming"
- beakColor (string) ex. pink, red, black...
- plumeColor (string) ex. pink, red, black...
- legsColor (string) ex. pink, yellow, white
- dim (tuples of int, one for X and one for Y)
- catchingFoods (list of string) 
- life (int, the number of hits for catch)
- scoreHit (int) ex. from 1 to 10 or 20. 