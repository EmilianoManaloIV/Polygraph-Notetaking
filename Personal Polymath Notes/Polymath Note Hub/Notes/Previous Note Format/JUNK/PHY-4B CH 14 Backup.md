___
* We have two loops of wire, where *$I_{1}$* is bigger than wire $I_{2}$, which there is $\Phi$ magnetic flux through wire $I_{2}$ 
$$E_{0}=-\left( \frac{d}{dt} \right)N_{2}\Phi_{12}$$
$$E_{1}=-\left( \frac{d}{dt} \right)N_{1}\Phi_{21}$$
* M is mutual inductance
*$$M_{12}=\frac{N_{2}\Phi_{12}}{I_{1}}$$
$$M_{21}=\frac{N_{1}\Phi_{21}}{I_{2}}$$
* Are they equal? If so, why?
	* Flux relies on the magnetic field and the area
	* Magnetic field relies on current.
$$\Phi_{12}=BA$$
$$= \frac{\mu_{0}I_{1}R_{1}^2}{2(y^2+R_{0}^2)^\left( \frac{3}{2} \right)} *A$$
* So in general what is $M$?
$$M=\frac{N_{2}\Phi_{12}}{I_{1}}=\frac{N_{1}\Phi_{21}}{I_{2}}$$
* So what is being induced? And therefore:
*$$E_{ind}=-\frac{d}{dt}(MI_{1})=-M\left( \frac{d}{dt} \right)I_{1}$$
* How does this relate to back $EMF$?
	* So when current goes around a loop of wire, it self induces a flux to itself
$$E_{ind}=\frac{d\Phi_{B}}{dt}$$
* This is called an inductor, which, opposes the change of current. This is because the inductor creates back EMF.
* So what is an RL (Resistor and Inductor) circuit?
* Loop Rule, see fig 1:
$$E-IR-L\left( \frac{dI}{dl} \right)=0$$
*Looks Like A Differential Equation*
$$E-R\left( \frac{dQ}{dI} \right)-\frac{Q}{L}=0$$

*Looks familiar to how capacitors operate on voltage or current*
$$I(t)=I_{ind}\left( 1-e^\left( -\frac{L}{t} \right) \right)$$
*So when it stops charging, it kinda looks like a capacitor discharging*
$$I(t)=I_{0}e^-\frac{L}{t}$$
* So what is a LC circuit?
	* Causes the circuit to "alternate" charges due to back EMF
* What about an RLC circuit?
	$$\frac{Q}{l}-l\left( \frac{dI}{dt} \right)-IR = 0$$
$$\frac{Q}{l}-R\left( \frac{dq}{dt} \right)-L\left( \frac{d^2q}{dt^2} \right)=0$$
* What is the differential equations?
*$$m\left( \frac{d^2x}{dt^2} \right)+b\left( \frac{dx}{dt} \right)+k_{x}=0$$
They are the same! Therefore:
$$Q(t)=Q_{0}e^\left( -\frac{t}{l} \right)\cos(wt+Q)$$

