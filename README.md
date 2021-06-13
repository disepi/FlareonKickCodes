# FlareonKickCodes
Flareon/Hive's anticheat kick codes, read below. These are not 100% correct.

# Abagnale
> Cause

This occurs when you login with EditionFaker. This flags when your game edition is not matching to your game editon in the LoginPacket that is sent when you join.

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

>Solution

Solution 1: Do not teleport up/down

Solution 2: Send a packet in the middle of the two positions you're teleporting to

