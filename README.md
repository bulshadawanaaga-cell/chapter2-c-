# chapter2-c-
1. TextBox Control

TextBox waa control u oggolaanaya user-ka inuu keyboard-ka ku geliyo xog. Default name-ku waa textBox1, textBox2, iwm. 

Text Property

textBox1.Text = "Hello";

In la nadiifiyo:

textBox1.Text = string.Empty;

ama:

textBox1.Clear();

ama:

textBox1.Text = "";

Text property waxay kaydisaa input-ka user-ka, waxayna tahay string. 


---

2. Variables ⭐⭐⭐

Variable = meel memory-ga ah oo lagu kaydiyo data.

Syntax:

DataType VariableName;

Tusaale:

string name;
int age;
double salary;

Variable waa in marka hore la declare gareeyaa ka hor inta aan la isticmaalin. 

Variable naming rules

Waa inuu ku bilaabmaa letter ama _

Spaces lama isticmaali karo

Keywords/reserved words lama isticmaali karo

Magac macno leh isticmaal


Tusaale:

string studentName;
int studentAge;




---

3. String Variables ⭐⭐⭐

string waxaa lagu kaydiyaa characters/text.

string university = "Jamhuuriya University";

MessageBox:

MessageBox.Show(university);

String Concatenation

+ waxaa lagu isku daraa strings.

string firstName = "Ibrahim";
string lastName = "Mohamed";

string fullName = firstName + " " + lastName;

Waxaad sidoo kale isku dari kartaa string iyo number:

string result = "Total is " + 25.75;




---

4. Local Variables & Scope ⭐⭐

Local variable = variable lagu declare-gareeyay method gudaheeda.

private void button1_Click(object sender, EventArgs e)
{
    string name;
    name = nameTextBox.Text;
}

Variable-kaas waxaa isticmaali kara statements-ka method-kaas oo keliya.

Scope = meesha program-ka variable-ka laga isticmaali karo.

Lifetime = muddada variable-ku memory-ga ku jiro. 


---

5. Initializing Variables ⭐⭐⭐

Variable waa in value loo assign-gareeyaa ka hor inta aan la isticmaalin.

❌ Khalad:

string name;
MessageBox.Show(name);

✅ Sax:

string name;
name = "Ibrahim";

MessageBox.Show(name);

Ama:

string name = "Ibrahim";

C# compiler-ku ma oggola local variable aan value loo assign-gareyn in la isticmaalo. 


---

6. Numeric Data Types ⭐⭐⭐

Kuwa ugu muhiimsan:

int       → whole numbers
double    → numbers with decimal parts
decimal   → precise decimal numbers, especially financial values

Tusaale:

int age = 20;

double temperature = 87.6;

decimal salary = 500.50m;



Decimal literal

Markaad decimal isticmaalayso, m ama M ku dar:

decimal price = 28.75m;




---

7. Type Casting ⭐⭐⭐

Casting = data type mid kale loogu beddelayo si explicit ah.

decimal money = 4500m;

int number = (int)money;

Ama:

decimal money = 625.70m;

double number = (double)money;

Syntax:

(DataType)variable




---

8. var Keyword ⭐⭐

var wuxuu compiler-ka u oggolaanayaa inuu isagu ogaado data type-ka.

var interestRate = 12.0;
var stockCode = "D465U";
var balance = 1000.0m;

Laakiin var waa in value lagu initialize-gareeyaa isla markiiba:

var age = 20;

❌:

var age;

var waxaa loo isticmaalaa local variables. 


---

9. Arithmetic Operators ⭐⭐⭐

+   Addition
-   Subtraction
*   Multiplication
/   Division
%   Modulus (remainder)

Tusaale:

int x = 10;
int y = 3;

int sum = x + y;
int difference = x - y;
int product = x * y;
int quotient = x / y;
int remainder = x % y;



Parentheses

result = (a + b) / 4;

Parentheses waxay kaa caawinayaan inaad si sax ah u maamusho order-ka calculation-ka. 


---

10. Integer Division ⭐⭐⭐

Haddii aad int / int sameyso, natiijadu waa integer.

int x = 7;
int y = 3;

MessageBox.Show((x / y).ToString());

Natiijadu waa:

2

Haddii aad rabto decimal result:

MessageBox.Show(((double)x / y).ToString());

ama:

double x = 7;
double y = 3;

MessageBox.Show((x / y).ToString());




---

11. Parse() ⭐⭐⭐⭐⭐

Aad muhiim u ah C# Windows Forms.

TextBox wuxuu input-ka u arkaa string, xitaa haddii user-ku qoro number.

Sidaas darteed:

int age = int.Parse(ageTextBox.Text);

double temperature = double.Parse(temperatureTextBox.Text);

decimal price = decimal.Parse(priceTextBox.Text);

Methods-ka muhiimka ah:

int.Parse()
double.Parse()
decimal.Parse()



Xusuusnow

TextBox → String
String → Number = Parse()


---

12. ToString() ⭐⭐⭐⭐⭐

Number markaad rabto inaad ku soo bandhigto Label/TextBox, waxaad u baahan tahay string.

double salary = 1550.0;

salaryLabel.Text = salary.ToString();

Ama:

int number = 123;

MessageBox.Show(number.ToString());

General format:

variableName.ToString()




---

13. Formatting Numbers ⭐⭐⭐

ToString() wuxuu number-ka u format-gareyn karaa siyaabo kala duwan.

number.ToString("N2");

N = Number

number.ToString("F2");

F = Fixed-point

number.ToString("C");

C = Currency

number.ToString("P");

P = Percentage

number.ToString("E3");

E = Exponential/scientific format. 


---

14. Exception Handling ⭐⭐⭐⭐⭐

Exception = error dhacaya inta program-ku socdo.

Examples:

Dividing by zero

Invalid user input

File aan jirin oo la isku dayo in la furo


Haddii exception aan la handle-gareyn, program-ku wuu istaagi karaa. 

try-catch

try
{
    // code that may cause an error
}
catch
{
    // code that handles the error
}



Example

try
{
    double miles;
    double gallons;
    double mpg;

    miles = double.Parse(milesTextBox.Text);
    gallons = double.Parse(gallonsTextBox.Text);

    mpg = miles / gallons;

    mpgLabel.Text = mpg.ToString();
}
catch
{
    MessageBox.Show("Invalid data was entered.");
}


---

15. catch (Exception ex) ⭐⭐⭐

Waxaad heli kartaa fariinta error-ka:

try
{
    // code
}
catch (Exception ex)
{
    MessageBox.Show(ex.Message);
}

ex.Message wuxuu soo bandhigayaa default message-ka exception-ka. 


---

16. Named Constants ⭐⭐⭐

Constant = value aan la beddeli karin inta program-ku socdo.

Waxaa lagu sameeyaa const.

const double INTEREST_RATE = 0.129;

Tusaale:

const double PI = 3.14159;

Uppercase waa convention caadi ah, laakiin khasab ma aha. 


---

17. Fields ⭐⭐⭐

Field = variable lagu declare-gareeyo class level, laakiin aan method gudaha lagu declare-gareyn.

public partial class Form1 : Form
{
    private string name = "Charles";

    // methods...
}

Field-ka waxaa isticmaali kara methods-ka class-ka.

Local variable: method gudaheeda.

Field: class gudaheeda. 


---

18. Math Class ⭐⭐⭐⭐⭐

Kuwa imtixaanka aad muhiimka ugu noqon kara:

Math.Sqrt(x)

→ Square root

Math.Pow(x, y)

→ x raised to power y

Math.Max(x, y)

→ Greater value

Math.Min(x, y)

→ Smaller value

Math.Round(x)

→ Rounds number

Constants:

Math.PI
Math.E



Examples

double result = Math.Sqrt(25);

Result:

5

double result = Math.Pow(2, 3);

Result:

8


---

19. Focus & Tab Order ⭐⭐

Focus = control-ka hadda helaya keyboard input-ka.

Tab Order = order-ka controls-ku focus-ka u helayaan marka user-ku Tab riixo.

TabIndex wuxuu tilmaamaa position-ka control-ka.

First control → TabIndex = 0
Second control → TabIndex = 1
Third control → TabIndex = 2



Focus si code ah:

nameTextBox.Focus();




---

20. Access Key ⭐⭐

Button waxaad siin kartaa keyboard shortcut adigoo & gelinaya Text property.

Tusaale:

&Exit

User-ku wuxuu isticmaali karaa:

Alt + X




---

21. Colors ⭐⭐

BackColor → background color

ForeColor → text/foreground color

messageLabel.BackColor = Color.Black;
messageLabel.ForeColor = Color.Yellow;




---

22. GroupBox vs Panel ⭐⭐

GroupBox

Container ayuu yahay

Title ayuu yeelan karaa

Text property ayuu leeyahay


Panel

Container ayuu yahay

Title ma laha

Text property ma laha

BorderStyle ayaa loo isticmaali karaa





---

23. Logic Errors & Debugging ⭐⭐⭐⭐⭐

Logic error = program-ku wuu run-gareynayaa laakiin natiijada waa khaldan tahay.

Examples:

Wrong mathematical calculation

Value khaldan oo variable loo assign-gareeyo

Variable khaldan oo value loo assign-gareeyo


Visual Studio wuxuu leeyahay debugging tools lagu raadiyo khaladaadkaas. 

Breakpoint

Breakpoint = line code ah oo aad program-ka ku joojinayso si aad u eegto values-ka.

Marka program-ku gaaro breakpoint:

Program → pauses
        ↓
You examine variables
        ↓
Find the error



Single-Stepping

Code-ka waxaad u fulin kartaa hal statement mar kasta.

Shortcut:

F11

Waxaa lagu heli karaa line-ka khaladka keenaya. 


---

🔥 Code-ka ugu muhiimsan ee aad xafidi lahayd

// Variable
string name = "Ibrahim";
int age = 20;
double salary = 500.50;
decimal price = 25.50m;

// TextBox input
string name = nameTextBox.Text;

// String → int
int age = int.Parse(ageTextBox.Text);

// String → double
double salary = double.Parse(salaryTextBox.Text);

// String → decimal
decimal price = decimal.Parse(priceTextBox.Text);

// Number → String
label1.Text = age.ToString();

// Formatting
label1.Text = salary.ToString("C");
label2.Text = salary.ToString("N2");
label3.Text = salary.ToString("F2");
label4.Text = salary.ToString("P");

// Calculation
double result = (a + b) / 2;

// Exception handling
try
{
    int number = int.Parse(textBox1.Text);
}
catch
{
    MessageBox.Show("Invalid input.");
}

// Exception message
catch (Exception ex)
{
    MessageBox.Show(ex.Message);
}

// Constant
const double INTEREST_RATE = 0.129;

// Math
double root = Math.Sqrt(25);
double power = Math.Pow(2, 3);
double maximum = Math.Max(10, 20);
double minimum = Math.Min(10, 20);
double rounded = Math.Round(5.6);

// Focus
nameTextBox.Focus();

// Colors
label1.BackColor = Color.Black;
label1.ForeColor = Color.Yellow;
