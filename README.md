# Redirecting-the-scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
### Step 1:
Open the unity engine.

### Step 2:
Create a new plane and create a cube and give color for the cube.

### Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

### Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

### Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting.

### Step 6:
Next Create a another new scene named as page2.

### Step 7
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

### Step 8:
Click the Build and run button in the Build settings and run the scene.

### Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is page2.

## Program:
#### NAME : JANANI R
#### REGISTER NAME : 212221230039
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
public class PlayerController : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            SceneManager.LoadScene("scene2");
        }
    }
    private void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "object")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
```
## Output:
![ARVR1](https://github.com/Janani-2003/Redirecting-the-scene/assets/94288340/beff288d-e96b-485d-8f93-6f3c970bedc3)
#### after ball hitting the cube:
![ARVR2](https://github.com/Janani-2003/Redirecting-the-scene/assets/94288340/006a9d14-5a4b-4dd1-b18a-20a26446e227)
#### Redirected scene:
![ARVR3](https://github.com/Janani-2003/Redirecting-the-scene/assets/94288340/c5a519a7-8989-4a5f-8ca5-4c72a9685429)


## Result:
Thus the above C# coding is successfully redirecting the scene in the unity engine.
