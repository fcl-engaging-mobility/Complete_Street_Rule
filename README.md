# Complete_Street_Rule
This is an updated repository for a modified version of the ESRI Complete Street rule by the original rule author. 
The rule uses the original assets folder of the ESRI Complete street rule, so in order to use it, you really only need the updated CGA file. 
![alt tag](https://geonet.esri.com/servlet/JiveServlet/showImage/102-6915-27-160154/RoadDiet6.jpeg.jpg)
The rules new features include: 

Key changes to the rule include:

1. Best Fit setting allows the rule to make sure that the street has the option to not have exact geometry.
This still needs to be tested more so please comment if you have any issues with the rule. The best fit feature works by calculating empty space and then adding it to the lane width. This means that your lane width attribute becomes the minimum width the lanes can take on before it subtracts lanes.

2. Renamed reporting and creates subclasses to support new Dashboards in 2015.2.

3. Modal Preference replaced LTS rank

4. Added Mode Area reporting and dashboards to the street rule. Get percentage area dedicated to each mode for different designs.

5. Sample Dashboard Text included in project

6. Improved Default LOD Settings: If LOD is set to High, the street will now pick default population parameters to make the street seem occupied. LOD Settings are now Low (Asset choice changes to reduce polygon count), Moderate (high poly assets/choices), and High (high poly assets and populated streets).

7. Addition of Complete_Street_Simple.CGA: This additional included rule has about ~50 fewer attributes while maintaining the core functionality of the rule. This rule is intended to make demos or charrettes a little easier.

8. Addition of Sharrows: Added support for sharrows (shared use lanes). The sharrows only appear on the curb lane.

9. Addition of Mode Focused Thematics: Allows a user to highlight specific improvements to a street with custom color choices. For example, if you add a bike lane and select "Bicycle Highlight" thematic, the solid color attribute will only highlight added bike lanes. Also, the addition of a All Mode Preference option helps visualize all the mode preference reports at once.  

10. Other miscellaneous changes.

	-Dead end exception, dead ends, treated like they have a connection (for singular cross sections).

	-Fixed striping bug in right most lane that occurred as a result of floating point arithmetic/rounding error (a micro-lane is being created).

	-Fixed various aspects of the Bike Stress Ranking to deal with parking and cycle tracks.

	-Fixed how multimodal lanes handle non-intersections-the last stamps will not be added when they connect to joints and other "non-stop" neighbor shapes.

	-Better default planting widths for sidewalks: Sidewalk planting width was changed to mimic general guidelines and suggestions from a NACTO Tree Maintenance Guidelines Document. If you have a narrow sidewalk, the planting strip will narrow to a minimum of 2 feet, and grow to a maximum of 6 feet.
