# SimudyneProject


The Use case is to develop  an algrithm or a platform for Iterative data mining .

The Sample data set which is a file storage contains fields like 

Agent_Breed,Policy_ID,Age,Social_Grade,Payment_at_Purchase,Attribute_Brand,Attribute_Price,Attribute_Promotions,Auto_Renew,Inertia_for_Switch

Brand_Factor		
INPUT - Range (0.1 -> 2.9)		
		
Run for 15 Years		
Every Year:	Increment Age	
	If Auto Renew - Maintain Breed	
		
Else No Auto-Renew:	Affinity = 	Payment_at_Purchase/Attribute_Price + (2 * Attribute_Promotions * Inertia_for_Switch)
	
  If Breed_C	: Switch to Breed_NC if Affinity < (Social_Grade * Attribute_Brand)
                                      : if not keep the same 
  
	If Breed_NC	:Switch to Breed_C if Affinity < (Social_Grade * Attribute_Brand * Brand_Factor)
		                                  : if not keep the same 
 Output:	Agents in each Breed	
	Breed_C Lost (Switched to Breed_NC)	
	Breed_C Gained (Switch from Breed_NC)	
	Breed_C Regained (Switched to NC, then back to C)	
