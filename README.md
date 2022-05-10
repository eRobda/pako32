# pako32
One big dll buffed with classes and functions for making cheats in c#

## PakoAtuh

## PakoMemory

## PakoCPU

## PakoMenu
PakoMenu is class in which you can find two methods: MakeMenu and MenuControll.

#### _MenuControll_
syntaxe: MenuControll(form which you want to affect, any key that will show and hide menu, any key that will close the menu and all threads). To use MenuControll you have to make new method and run it as a thread. Do it as shown:

#### _MakeMenu_
syntaxe: MakeMenu(form which you want to affect). It sets form to borderstyle none and set position to the left top corner. Do it as shown:


```
using System.Windows.Forms;
using pako32;
using System.Threading;

namespace WindowsFormsApp2
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
            
            //make the menu
            PakoMenu.MakeMenu(this);
            
            //make and start thread
            Thread th = new Thread(t);
            th.Start();
        }
        void t()
        {
            CheckForIllegalCrossThreadCalls = false;
            PakoMenu.MenuControll(this, Keys.Insert, Keys.Delete);
        }
    }
}
```
