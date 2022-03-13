# Fog-of-War
This is a simple fog of war. <br />
When player moves, minimap will be revealed with radius 20. <br />

Procedure :
- Set up 2 Planes : Default Plane and Unexplored Plane
- Set the Unexplored Plane to black (check Initialize() in MapReveal.cs)
- On each update, make a raycast and reveal everything inside radius 20 :  
  (make the alpha to Mathf.min(meshColors[i].a, distance/radius^2)

Important : 
- Set the unexplored plane layer to "Unexplored"
- Set the default plane to "Level"
- Make the minimap camera to render "Unexplored" (Culling Mask)
