

### SO what are tensors 

- Tensor is a data structure
- Tensor is a container for numbers
- Matrix or Vector are also tensors

0D Tensors/Scaler

```python
import numpy as np
a = np.array(4)
a

a.nd

```

[ 1,2,3,4 ]  = 1D tensor/vactor (axis =1) vector have 4 dimensions 


2D = No of axis = no of dimension


1D tensor is a vector but the dimension of that vector is the elements in that vector

![[Pasted image 20251106145433.png]]



ND Tensors :
 ![[Pasted image 20251106145616.png]]

0-5D tensors
- Rank / Axis  and Shape:
- No of axis = Rank = No of Dimension
- Shape is depend upon the row * col
- Shape will give the no of items as row * column

#### Example of 1D Tensors

- Students (10000)
- CGPA/IQ/State/Placement
- 8.1/91/WB/1
- 7.2/102/Kr/0

![[Pasted image 20251106150010.png]]

tensor is 1d but dimension of vector can differ as in this example it is a 1d Tensor


### Example of 3D Tesnors NLP

Hi Harivansh
Hi Rahul
Hi Ankit


 | Harivansh | Rahul | Ankit

| HI  | Harivansh | Rahul | Ankit |
| --- | --------- | ----- | ----- |
| 1   | 0         | 0     | 0     |
| 0   | 1         | 0     | 0     |
| 0   | 0         | 1     | 0     |
| 0   | 0         | 0     | 1     |

3 2D tensors become 3D tensor

![[Pasted image 20251106153024.png]]




## Example of 3D tensor

Time Series Data

Highest price , Lowest Price data per day for stock price




![[Pasted image 20251106153113.png]]


you get the 2d tensors but if you try to get data for 10 years it means  10 different 2d tensors then we will have a 3d tensors with (10, 365 , 2)

#### D tensors : Image based data 


for image proceessing we have pixels and in pixel we have numaric values
and if we want to give the colors we have 3 type of colors but if we have a matrix of 1200* 800 pixel for one color and we have 3 colors then we have (3,1200,800) so if we have 50 color images then  we have (50 * 3 * 1200* 800) so we have 4D tensor here for working on the image based data 




### 5D  Tensors : Video Based Data

our persistence of vision only can classify 12 images per second , anything more then that appear to be a video 

in short videos is a collection of frames or images bind together one after another in a series

If we have a 60 second video with 30fps and 480p  means 480 * 720 px with rgb colors 
in one scond we have 30 images and in 60 second we have 1800 images 

(4*( 1800, 480, 720,3))


it will take around 27 Gb of space but for that we have video encoding formats which help us by fixing the storage and accessing issue and keep video lite and accessible 


students from sno. 1 to 25 sat sunday lacture hall 8 with dbda 9 to 12 aptitude classes from s no 24 onwards monday to friday 9- 10:30 on lacture hall 8 from tomorrow the technical classes will start from 10:40 on upcoming monday our python programming lab assesment will be schedule on 11:00 am and second half will be off on monday and tomorrow 13/november and the day after tomorrow 14/nov saruti gupta maam will take the class of Data Analytics all day