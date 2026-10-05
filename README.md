# GAME_PROGRAM-EX--4

Attach Rifle with character mesh and implementation bullet spawn from Rifle

## AIM:
To create an aiming system (attach and aim a rifle with a character) in Unreal Engine,you’re using a third-person character and a rifle skeletal mesh.

## Procedure:

1.Attach the Rifle to the Character Import the Rifle Skeletal Mesh into Unreal Engine. Open your Character Blueprint (e.g., BP_ThirdPersonCharacter). In the Components tab: Add a Skeletal Mesh or Static Mesh component (name it Rifle). Set its Skeletal Mesh to your rifle asset.

2.Attach the Rifle to a socket on the character’s skeleton: In the Rifle component, set the Parent Socket to something like hand_r (right hand socket). manually attach in Event Graph:

Rifle->AttachToComponent(Mesh, FAttachmentTransformRules::SnapToTargetNotIncludingScale, "hand_rSocket");

Add Aiming Mechanism Create a Boolean variable called IsAiming. Set up Input in Project Settings: Go to Edit > Project Settings > Input. Add an Action Mapping named Aim (e.g., Right Mouse Button).

Adjust Camera When Aiming Add a Camera Boom and Follow Camera.

In Event Graph:
When IsAiming = true, zoom the camera in (FOV) and slightly shift it over the shoulder.

## Output:
<img width="1038" height="837" alt="Screenshot 2026-10-05 202729" src="https://github.com/user-attachments/assets/a7fb5ac3-a7e0-4ccc-8ea3-d839a2daed1f" />

<img width="1041" height="637" alt="Screenshot 2026-10-05 202741" src="https://github.com/user-attachments/assets/72d21a95-4789-4f36-b863-185d1b1aa432" />



## Result:

Attach Rifle with character mesh and implementation bullet spawn from Rifle is successfully done.
