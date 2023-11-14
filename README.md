# Redirecting-the-scene

## Aim:
To Redirecting the scene in the unity engine.
## Algorithm:

# Step 1:
Open the unity engine.

# Step 2:
Create a new plane and create a cube and give color for the cube.

# Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

# Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

# Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting.

# Step 6:
Next Create a another new scene named as page2.

# Step 7:
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

# Step 8:
Click the Build and run button in the Build settings and run the scene.

## Program:
~~~
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
public class PlayerController : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
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
~~~
## Output:
![image](https://github.com/sasidharan403/Redirecting-the-scene/assets/94154712/61389c8e-8bfc-4aab-a524-9eebe0b83043)
![image](https://github.com/sasidharan403/Redirecting-the-scene/assets/94154712/864d8561-f59f-4cf5-aee6-820bbda6b99f)
![image](https://github.com/sasidharan403/Redirecting-the-scene/assets/94154712/25617a7a-af2f-46f1-bb2f-5a8bc7b2dd35)


## Result:
Thus the above C# coding is successfully redirecting the scene in the unity engine.
