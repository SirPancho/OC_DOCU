

# 1.- Transport element

1. Add a Transport linear component to the sub element Transport of the Prefab. If the transporting surface is not straight then a Transport curve can be inserted
2. Check the box of the *Gizmos* to display the edges of the collider box of the transport component
3. Adjust the size and position of the transport according to the geometry size
4. Add a Drive simple component to the sub element MA_Drive of the Prefab. The type of drive component to be added to the object depends on the type of drive with which the transport surface will be controlled.
5. In the Transport component set the actor to the recently added MA_Drive

**NOTE:** when creating a transport element, it is recommended that the transport object is alligned with the Z-Axis, this is by design the direction for FWD movement

![[Pasted image 20260715132132.png]]

Configure the acceleration of the drive to *infinity*


![[Drive_acceleration_config.png]]

# 2.- Payload element

1. In the main Project tree create a new Empty object called *POOL*
2. Add the Pool component to the Pool game object.
3. Insert the CAD file of the payload element into the project tree
4. Create a **Prefab** of the payload
5. Open the Prefab editor
6. Add a payload component to the Prefab
7. Adjust the size and the origin of the payload component based on the geometry. The origin of the payload should be in the bottom of the geometry and centred.

# 3.- Sensor element

If the Detection flag is going to move with a mechanical part of the Prefab, change the Physic state of the detection flag from Fee to Parent

If the Sensor is going to move and the detection flag is going to remain static, change the Physic state of the detection flag from Free to Static

![[Pasted image 20260715132123.png]]

# 4.- Linear actuator element

![[Pasted image 20260723133354.png]]


## Source (feed in payloads)

1. Create a cube as child of the #prefab
2. Rename the cube as *source*.

![[Pasted image 20260724151705.png]]

3. Position the cube where the #payload should be created.
4. Adjust the scale of the cube according to the size of the payloads and the area where they will be generated.
 
**NOTE:** The #payload will be generated at the origin of the source object and the origin of the pay load will be located with the origin of the source object.

![[Pasted image 20260724151722.png]]

![[Pasted image 20260724151817.png]]

**NOTE:** The selected material for the source cube is optional can be replaced as preferred.

5. To create a payload with the source object, the payload has to be defined as an element of the #Pool object. The #payload will be referenced with the *Type ID*. it can be defined directly in the #Prefab as a fixed value or at each instance in the #Scene.
6. If it is needed the source element can be set to create automatically #Payload. For this it is necessary to mark the check box *Auto Mode*. As long as the box collider of the source is free of detecting a #payload , it will create a new one.

![[Pasted image 20260724160922.png]]

## Sink (feed out payloads)

![[Pasted image 20260724151912.png]]

![[Pasted image 20260724151933.png]]

![[Pasted image 20260724152008.png]]

**NOTE:** The selected material for the sink cube is optional can be replaced as preferred.