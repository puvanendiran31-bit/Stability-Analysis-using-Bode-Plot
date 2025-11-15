# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```

## Output:
<img width="700" height="622" alt="image" src="https://github.com/user-attachments/assets/9d319644-23b5-47b8-bc2d-b516c753879a" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB.
Gain margin = 12.0
Phase Margin = 60.42
Gain crossover frequency = 0.907
Phase crossover frequency = 4.4721
The system is stable
