# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
```clc;
clear;
xn=[1 2 3 4 4 3 2 1];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
    for k=0:N-1;
    for n=0:N-1;  
    Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
    end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle=atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('Phase spectrum');
```
### CALCULATIONS:
<img width="759" height="1280" alt="image" src="https://github.com/user-attachments/assets/2823c113-a1a3-4509-b075-e0306806b513" />
<img width="758" height="1280" alt="image" src="https://github.com/user-attachments/assets/b95e56b0-6c49-47a8-8ab4-dbc6c322f1bc" />
<img width="791" height="1280" alt="image" src="https://github.com/user-attachments/assets/fa069981-60de-44ba-8b02-6f00b19b247a" />



### SAMPLE OUTPUT:
<img width="756" height="715" alt="DFT dtsp" src="https://github.com/user-attachments/assets/aa0c7ff0-4927-4c84-8242-654cbe473753" />


## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.
