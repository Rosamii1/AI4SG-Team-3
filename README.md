# AI4SG-Team-3

(1) PROBLEM — Who is affected, and what specifically breaks down for them today? 
The problem we are tackling is sustainability of cities and communities in the Bay Area. There are many properties and buildings here in the Bay Area that have problems such as displacement, congestion, and high rent rates. These issues also contribute to increasing unaffordability of goods and services. These issues affect residents of the Bay Area and nearby regions, particularly the working class and middle class. We aim to provide an AI program that can help identify potential land-use issues with a particular plot and suggest improvements, allowing for a conversation with the user that aims to inform.

(2) AI CAPABILITY — Which lab capability addresses the failure point, and why does it fit? 
For our project, we wanted to make the AI capable of reading both user text and image input in order to analyze the info provided, whether it’s in text or image form. Due to Gemini API constraints, we were only able to make the AI capable of reading a screenshot of a location provided amongst a satellite map (like Google Maps) and analyzing the info stored in that map. With the capability of uploading and reading a screenshot of a location, lab 3 was able to address and work around the failure point.

(3) WORKFLOW — what goes in, what the AI does, what comes out, and who acts on it, including screenshots 
Lab 3: What goes into the AI is image and user input. When first uploading an image, the AI will use the info provided in the image and convert it into a variable for the code to use. Then it will display the uploaded image.

Lab 3: If the AI is unclear of what location needs to be used, the user can input the desired location among the map when the AI asks, “Please specify the location on this map.”


Lab 3: The AI will then analyze the image in a for loop by finding the image’s filename and applying the analysis into each question provided in a list of pre-written questions.

Lab 1: Finally, the program enters into a continuous loop where the user may ask any follow-up question. The algorithm we used specifically uses the AI’s previous answer, rather than the source image itself, as we found it somehow provided more reliable and accurate results.



(4) FAILURE CASE — One specific failure, with a reference to the lab output that showed it is possible.
One failure case that was most prominent in our lab was the AI not being able to provide real-time info about our location. It ended up hallucinating lots of info, such as street names, the land owners, the city where the land is located, etc. This actually led to us needing to change the scope of our project, as we discovered the AI’s limitations would not allow us to implement our original plan as envisioned.

For example, originally, when we had the user text input and asked about the exact coordinates of a location. The AI was not able to correctly identify the location of the coordinates. Instead it would spit out random information unrelated to the location we selected. Our selected location is nowhere near the Berryessa neighborhood, nor Senter Road or Monterey Road. It would give different random locations as it cycled through the civic questions.

(5) OVERSIGHT AND TRADEOFF — Where does human review sit, and what does the one change cost?
When we realized the AI would not give us real-time info on our location, we changed our thinking. Initially we thought we would use the AI to analyze street-level view images of locations and it would search it up on a real-time map. However, this would routinely fail, with the AI providing verifiably false information. The same was true for text-only prompts, another feature we initially intended to incorporate. The AI would fail to understand the location being asked about even when given exact GPS coordinates. The only reliable way to get the AI to correctly determine the exact location was to have it analyze satellite map screenshots, which meant that users would have to go to a satellite map, such as Google Maps, to take a screenshot of the location they are trying to learn more about. The trade-off here was that our AI was limited to extracting more info from a map than it would be from a surface-level image of a location, however, this allowed the AI to stop hallucinating results and provide more accurate information about our location.
