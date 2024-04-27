# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:ARIVAZHAGAN G R
RegisterNumber:*/212223040020
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming.


module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and g1(s,ydash,z);
and g2(t,x,y);
and g3(u,w,z);
or g4(f2,s,t,u);
endmodule


**RTL realization**
![322416806-a86b8a88-9cfd-46f7-a430-98227cff9fc4](https://github.com/ARIVAZHAGAN04/BOOLEAN_FUNCTION_MINIMIZATION/assets/161414455/8f81d78f-64fa-4295-acef-afaff9cfa6fa)




**Output:**

**RTL**
![322416962-52e5be68-d7b5-4f48-ad95-1b8848c327ec](https://github.com/ARIVAZHAGAN04/BOOLEAN_FUNCTION_MINIMIZATION/assets/161414455/586d8b3f-718c-4a70-b323-bfb20efff0db)

**Timing Diagram**
![322417168-82dea792-3035-42b6-af5c-134c0e74c8b2](https://github.com/ARIVAZHAGAN04/BOOLEAN_FUNCTION_MINIMIZATION/assets/161414455/371dc7a4-fac9-4a03-9108-22d7518cc9d8)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

