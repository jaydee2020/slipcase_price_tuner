# slipcase_price_tuner

A notebook containing a simple tool to be used by a manufacturer to fine-tune pricing calculations.

The business problem:<br> 
A manufacturer of custom boxes for packing fine art found that the price calculator on their e-commerce site produces undesirable results in extreme cases. The calculator programatically generates a price based on a customer's input of dimensions. But because the calculator uses a simple linear-inch model, prices "feel" too high for very small boxes and too low for very large boxes. Additionally, prices grow too rapidly when square- or cubic-inch models are used instead for the calculator. The manufacturer is generally happy with the liner-inch model and asked for a way to modify the prices in the extremes.

The solution:<br>
I created a pricing grid visualization in a Colab notebook and wrote exponential expressions to selectively raise or lower prices based on the size of the box. The underlying price model remains the same but coefficients can be adjusted to independently target quadrants in the grid. The manufacturer can experiment with combinations until the prices of small and large boxes feel right without affecting the midsize box pricing. The notebook generates a PHP code version of the corresponding expression which the manufacturer can copy and paste into the price-calculation field in their e-commerce site.
