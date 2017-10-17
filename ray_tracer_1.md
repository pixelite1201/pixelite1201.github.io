#RayTracing

##CS775ComputerGraphics-Assignment1Part1

***

WehaveimplementedRayTraceraspartofourassignment.ItcancreateaScenewithsphere,coneandcylinder.Itcanalsoenable3materialpropertiestothemviz.Diffuse,ReflectiveandReflective+Transparent.ItshowstheinteractionofLightrayswiththem.ItalsoallowtoRenderScene,withLightSourceatdifferentLocation.
[<fontsize="3">ProblemStatment</font>](http://www.cse.iitb.ac.in/~paragc/teaching/2014/cs775/assignments/A2/A2.pdf)

###CodeDescription

**render.cpp**

*ContainParsertoparsethescenefile
*Calculateintersectionpointandnormalwithobjectatminimumdistance.
*Ifobjectisdiffuse,thenfindwhetherraycanreachthelightsource.Ifitcan,assigncolortoobjectelseitsinshadow.
*Ifobjectisreflectiveortransparent,simplereflectionandrefractionareperformed,andtheaggregatedcolor,weightedbyFresnelRationisappliedtotheobject.
*Ifaliasingison,thenitwillperform4xsupersampling.

**object.cpp**

*FunctiontocalculateintersectionpointofRaywithSphere,CylinderandCone.
*FunctiontocalculateNormalofSphere,CylinderandConeatpointofintersection.
*FunctiontofindwhetherRayoflightintersectwithanyobject.

**vector.cpp**
LightRays,Positions,Normaletc.aredenotedasVectors.ContainsutilityfunctiontoperformvariousoperationonVectors.

###ScenefileDescription

**Image:Width,Height**
640480
**Resolution:Width,Height**
640480
**Camera:Near,Far**
1200
**FieldofView**
40
**LookAtVector**
00-1
**Vup**
010
**Cop**
4930
**ObjectCount**
2
**Objectspecs(0:Sphere,1:Cylinder,2:Cone,Color(0,0,0),transp,reflect,Dimensions,location)**
**Sphere**
0
**Color**
00255
**TransparentReflectance**
00
**Radius**
2
**Center**
13-2
**Cylinder**
1
**Color**
02550
**TransparentReflectance**
11
**Radius**
3
**Height**
6
**Basecenter**
42-3
**Lightsrc(count:location)**
**NumberofLightSource**
2
**LocationofLightSource**
578
-23-4
**Anti-aliasing(on/off)**
0
**Ambientcomponent(on/off)**
0

###OutputImages

![](shadow1.jpg)![](shadowours.jpg)![](smoothours.jpg)![](shadow4.jpg)![](normal1.jpg)![](normalscene2.jpg)![](normal3.jpg)![](normal4.jpg)

###Acknowledgement

1.[SimpleRaytracer](http://www.scratchapixel.com/lessons/3d-basic-lessons/lesson-1-writing-a-simple-raytracer/)
2.[ForCalculatingNormals](http://www.ctralie.com/PrincetonUGRAD/Projects/COS426/Assignment3/part1.html)
