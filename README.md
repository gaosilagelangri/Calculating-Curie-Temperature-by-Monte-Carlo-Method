# Calculating-Curie-Temperature-by-Monte-Carlo-Method

To calculate the Curie temperature it is in fact only necessary to know the following parameters：

+ J
+ D
+ Direction
+ Patience

My Enlightenment [Video](https://www.bilibili.com/video/BV1jZ4y1T7Ds?from=search&seid=6713171886036134943)，The downside is that the video has no sound and is not detailed enough, but it solves a lot of problems！Thanks lot for it.

I use Monte Carlo Method to calculate and use the Open Source Programs [**MCSOLVER**](https://github.com/golddoushi/mcsolver)!I discussed its use with its author（PhD.Liang Liu） and became familiar with its use!Following,I'll explain the usage in detail！

Usually I start by editing all the parameters under Windows，then I exported the input file to run under Linux.

The general interface of the program is as follows：

<img width="500" alt="Fig1.png" src="https://github.com/Nick12-hub/Calculating-Curie-Temperature-by-Monte-Carlo-Method/blob/main/Fig1.png">

Now I explain all parameters one by one.

## Lattice

In general，a1(1.0 0.0 0.0),a2(-0.5 0.866 0.0),a3(0.0 0.0 1.0).
### SC(SuperCell) 

It depends on whatever you want to choose,it maybe takes dozens of differences.

## Orbital List

ID is beginning at 0 and you need to write out the positions of all unequal atoms in the smallest cell.Spin depends on your system（This parameter is simple to determine but error-prone）.If you consider **D**, you need to fill in the parameters for the z-direction. Maybe it has a small effect, but you need to test it.
You can use this formula to estimate:

```
$D=\frac{E_{\mathrm{FM}}^{\beta}-E_{\mathrm{FM}}^{z}}{4 S^{2}}$
```

## Bond List




