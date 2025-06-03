# Manipulation relationship identification based on monocular visual deformation field

### This idea involves voxel transfer within the full frame range of a continuous image frame of a single camera. Another description is the deformation field within the entire field of view. It doesn't matter. We can gradually understand what it is. In short, this passage is to introduce to you a kind of perceptual information source that I think has great application potential.

## Source of idea

In laparoscopic surgery, often only one lens extends into the surgical area, and there are no other sensors (power-off sensors, radars, contact buttons) besides that. 

So how do surgeons perceive the situation of the area to be operated on? In addition to their prior surgical experience, they attempted to touch the tissues, observe their deformations, and conduct depth positioning, mechanical property analysis, boundary parameter analysis, etc. During this process, the surgical instruments are the objects controlled by the doctor. Their appearance in the laparoscope is completely in line with the doctor's operational intuition, that is, they always move along with the operation. And doctors further help perceive information from the transfer relationship between the image of the instrument and the image of the tissue. More specific examples:

* Two-dimensional images have no depth information. To locate the depth distance of the tissue, the doctor slowly penetrates the instrument until deformation occurs at the junction of the instrument and the tissue in the image, that is, the instrument sinks into the tissue. Then it can be determined that the depth at the end of the instrument at this moment is the depth of the tissue.
![](image/touch.png)

* The electric hook is used to burn separated tissues. After the doctor operates the electric hook to hook the tissue, they will step on the electric pedal. Then, the part of the tissue that has been hooked will be damaged by the hot electric hook. So how do doctors determine if an organization has been hooked? Obviously, they observed whether the tissue near the electrohook in the two-dimensional image moved along with the electrohook. If the movement is completely synchronized, that is precisely the part held by the electric hook. If it is partially synchronized, then it might be a transitional part. If it has nothing to do with the movement of the electric hook at all, then it must not have been involved.
![](image/hook.png)

* We mentioned the boundary parameter earlier. What is it? Let's understand it with the work of UCSD:
![](image/boundary.png)
Simply, boundary parameters refer to whether two or more organizations are adhered to each other, or exactly where and to what extent they are connected. Its significance in surgery is not only to discover the position to be cut, but also to achieve more flexible and efficient operation. For example, in cholecystectomy, doctors often do not use two instruments to separate the liver and the gallbladder respectively. Instead, they only need one instrument to separate the gallbladder and push it backward. This is that after clarifying the boundary parameters between the liver and the gallbladder, one operation is sufficient to fix the two organs.