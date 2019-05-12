# arwa
my project
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

public partial class Welcom : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {

    }
    protected void Button1_Click(object sender, EventArgs e)
    {
        //Name 
        if (TextBoxName.Text == "")
        {
            Label1Name.Text = "Not fulfill the requirments";
        }
        else
        {
            TextBoxName.Text = TextBoxName.Text.ToUpper();
            Label1Name.Text = "Fulfill the requirments";
            Label7.Text = "Dear " + TextBoxName.Text + " for your application";
        }

        //Nationality
        if (list1Nationality.SelectedItem.Text == "Omani")
        {
            Label2Nationality.Text = "Fulfill the requirments";
        }
        else if (list1Nationality.SelectedItem.Text == "Saudi")
        {
            Label2Nationality.Text = "Not fulfill the requirments";
        }
        else if (list1Nationality.SelectedItem.Text == "indian")
        {
            Label2Nationality.Text = "Not fulfill the requirments";
        }

        //Age
        int age = Convert.ToInt16(TextBoxAge.Text);
        if (age < 15 || age > 30)
        {
            Response.Write("<script>alert('Should be between 15-30 years old');</script>");
        }
