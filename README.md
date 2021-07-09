# FlareonKickCodes
Flareon/Hive's anticheat kick codes, read below. These are not 100% correct.

# Note

Kick messages are disabled with the new anticheat update in Skywars and Treasure Wars. Any other game still has these kick messages!

# Abagnale
> Cause

This occurs when you login with EditionFaker. This flags when your game edition is not matching to your game edition in the LoginPacket that is sent when you join.

> Solution

Solution 1: Either spoof the edition in the LoginPacket or revert EditionFaker changes.

# Bluebird
> Cause

This occurs when you teleport too far/too near or go too fast.

> Solution

Solution 1: Lower the speed to 0.23f lower in player speed.

Solution 2: Only teleport 2.3 blocks at a time.

Solution 3: Teleport the same amount of blocks at a time.

Solution 4: Increase the teleport range (20 blocks range is the sweet spot)

Solution 5: Do not set your position to null in MovePlayerPackets.

# SugarRush
> Cause

This occurs when you break more than one block in 1 tick.

> Solution

Solution 1: Increase delay between breaking blocks by 20ms.


# Woodpecker
> Cause

This occurs when you are inside a block.

> Solution

Solution 1: Do not send MovePlayerPackets while inside blocks.

# Bluebord
> Cause

This occurs when you move too fast while walking sideways/backwards.

> Solution

Solution 1: Lower speed while not moving forward.

Solution 2: Don't sprint sideways/backwards.

Solution 3: Change bodyYaw and yaw inside MovePlayerPackets to match your movements.

# Cyanbird
> Cause

This occurs when you teleport up/down too high/low.

> Solution

Solution 1: Do not teleport up/down.

Solution 2: Send a packet in the middle of the two positions you're teleporting to.

# CIA
> Cause

This occurs when you attack too fast/attempt to attack an entity not in your field of view too many times or attack an invalid entity (bots).

> Solution

Solution 1: Add a delay before attacking.

Solution 2: Edit/send MovePlayerPackets that have the pitch & yaw & bodyYaw pointing at the entity.

Solution 3: Do not attack bots (item shop bots, immobile players etc.)

Solution 4: If using hitbox, make hitbox size smaller.

# Platinumo
> Cause

This occurs when you are not falling while not on ground. Similar to Element1 check.

> Solution

Solution 1: Find a way to make a server think you're on ground.

Solution 2: Do not float with a very low vertical velocity.

Solution 3: Do not float upwards.

# Orangebird
> Cause

This occurs when you move too fast/slow while in air.

> Solution

Solution 1: Match the speed you're going at to sprinting speed.

Solution 2: Do not shift X/Z velocity while in air.

Solution 3: Stay onground

# JFEM3D
> Cause

This occurs when you teleport to a position and then teleport back from where you teleported from.

> Solution

Solution 1: Teleport back to the same position except with a 1 block difference to the X/Z position of the MovePlayerPacket.

# BP-219
> Cause

This occurs when you send too many/not enough MovePlayerPackets or sent the same MovePlayerPacket more than once.

> Solution

Solution 1: Do not send extra MovePlayerPackets or try to cancel them.

Solution 2: Change the position/angles in the MovePlayerPacket by a small value.

Solution 3: Do not move while sending no packets.

# Element1
> Cause

This occurs when you are not falling while not on ground. Similar to Platinumo check.

> Solution

Solution 1: Set onGround in outgoing MovePlayerPackets to true.

Solution 2: Do not glide.

Solution 3: Find a method to make the server think you're onGround.

Solution 4: Do not change velocity while falling.

# Platinum
> Cause

This occurs when you teleport in packets or not match other packets or not match server position to client position.

> Solution

Solution 1: Teleport clientsidedly.

# 400
> Cause

This occurs when you tamper with packets.

> Solution

Solution 1: No real solution.

# 403
> Cause

The cause of this has not been 100% found. This could be changing onGround while in the packet.

> Solution

Solution 1: Do not change onGround in packet when not needed.

Solution 2: Always make onGround in packets true.

# 404
> Cause

This occurs when you change velocity while midair.

>Solution

Solution 1: Keep the velocity at a static value while midair.

Solution 2: Set onGround in outgoing MovePlayerPackets to true.

# 405
> Cause

This occurs when you attack without sending a swing animation packet. This flags bad killauras (toolbox)

> Solution

Solution 1: Call the swing function in LocalPlayer.

Solution 2: Send swing animation packets.

Solution 3: Delay before attacking is too low, this will false if you attack too fast!

# SPE-90
> Cause

This is a more strict Platinumo/Element1 check.

> Solution

Solution 1: Do not glide.

Solution 2: Set onGround in outgoing MovePlayerPackets to true.

Solution 3: Find a way to make the server think you're on ground.

# SFF-90
> Cause

This is a more strict Element1/Platinumo/SPE-90 check. The actual cause is not known, it may be checking if you haven't changed your Y position in a while, if the block below you has been air for too long etc.

> Solution

Solution 1: There is no solution to this.

# Internal server error
> Cause

You either sent way too many packets or sent invalid packets. The server could not handle your packets.

> Solution

Solution 1: Either check the validity of outgoing packets or do not attack too fast.
