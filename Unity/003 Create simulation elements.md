

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
