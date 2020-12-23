# ARCSgeometry
The ARCS Geometry is created using the following output file type.

## Required Packages
The following packages are required to use run this code: airfoil_db, numpy, json, scipy, and shapely. The airfoil_db package can be found [here](https://github.com/usuaero/AirfoilDatabase).

## Running the Code
The code can be run by importing the code and running the main function with a single input of the input formatted JSON file location.

## Input File Format
The input file should have a dictionary with the key "C14". The following keys and corresponding types should be in the "C14" dictionary.

>**"airfoil dat file location" : string**
>>The airfoil dat file to be used for the ARCS geometry. It must be in Selig format, with no text before the airfoil data.
>>
>**"chord [in]" : float**
>>The airfoil chord length in inches.
>>
>**"num arcs" : integer**
>>The number of arcs desired in the geometry. must be greater than or equal to 1.
>>
>**"arc concave" : boolean**
>>Whether to create the arcs concave (true : arcing toward the trailing edge), or convex (false : arcing toward the leading edge).
>>
>**"arc type" : string**
>>Which type of arc to create. The options and corresponding descriptions are:
>>>"exponential"
>>>
>>>Create the arcs as having radii inversely increasing from the leading edge toward the trailing edge. The corresponding radius at the hinge point will be 
>>

"arc type" : "exponential",
"arc type notes" : "'exponential','reversed_exp', '90%t', or 'hinge_point'",
"section resolution" : 400,
"shell thickness [mm]" : 0.8,
"flex start [x/c]" : 0.5,
"tongue start [in]" : 1.0,
"tongue start [in]_notes" : "distance before flex start",
"mouth start [in]" : 2.0,
"mouth start [in]_notes" : "distance before flex start",
"TE wall start [x/c]" : 0.95,
"mouth clearance [mm]" :  1.0,
"fillet side length [mm]" : 1.0,
"enthicken" : 1.0,
"Notes" : " ",
"skip wing box" : true,
"show plot" : true,
"write dxf" : false,
"shift to c/4" : false,
"split return" : false,
"guide curve return" : false,
"actuation hole return" : false,
"show legend" : false,
"all black" : true,
"deflection angle [deg]" : [-15.0],
"deflection type" : "parabolic",
"deflection type notes" : "'none', 'traditional', or 'parabolic'",
"hinge at top" : true,
"dxf file path" : "/home/ben/Desktop/",
"dxf file name" : "c14"
