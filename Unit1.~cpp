//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma resource "*.dfm"
TForm1 *Form1;

//---------------------------------------------------------------------------
__fastcall TForm1::TForm1(TComponent* Owner)
        : TForm(Owner)
{
}
//---------------------------------------------------------------------------
void __fastcall TForm1::FormCreate(TObject *Sender)
{
           ;
}
//---------------------------------------------------------------------------
void __fastcall TForm1::BitBtn1Click(TObject *Sender)
{
  RichEdit2->SelectAll();
  RichEdit2->Font->Name = "MS Sans Serif";
  RichEdit2->SelAttributes->Size = 24;
  RichEdit2->SelStart = 0;

    Edit1->Text = RichEdit2->Font->Name ;
    ComboBox2->Text = RichEdit2->Font->Size ;
}
//---------------------------------------------------------------------------

void __fastcall TForm1::RichEdit2MouseDown(TObject *Sender,
      TMouseButton Button, TShiftState Shift, int X, int Y)
{
      int poz, dl;
      if( Shift.Contains(ssDouble))
       {
               RichEdit4->Clear();

            poz = RichEdit2->SelStart;
            dl =  RichEdit2->SelText.Length();

           RichEdit2->SelectAll();
           RichEdit2->SelAttributes->Color = clBlack;

           RichEdit2->SelStart = poz;
           RichEdit2->SelLength = dl;

           RichEdit2->SelAttributes->Color = clRed;

             RichEdit1->SelectAll();
             RichEdit1->SelAttributes->Color = clBlack;

             RichEdit1->SelStart = poz;
             RichEdit1->SelLength = dl;

               Edit2->Text = RichEdit1->SelText.Trim();
               RichEdit4->Text = RichEdit1->SelText.Trim();
               RichEdit4->SelectAll();
               RichEdit4->SelAttributes->Size = StrToInt(ComboBox3->Text);
               RichEdit4->SelAttributes->Name = Edit1->Text;
               RichEdit4->SelStart = 0;

             RichEdit1->SelAttributes->Color = clRed;

           RichEdit2->SelStart = poz;
       }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::RichEdit2MouseMove(TObject *Sender,
      TShiftState Shift, int X, int Y)
{
   RichEdit2->SetFocus();
}
//---------------------------------------------------------------------------

void __fastcall TForm1::RichEdit1MouseMove(TObject *Sender,
      TShiftState Shift, int X, int Y)
{
   RichEdit1->SetFocus();        
}
//---------------------------------------------------------------------------

void __fastcall TForm1::BitBtn3Click(TObject *Sender)
{
    RichEdit1->SelAttributes->Color = clRed;
    RichEdit2->SelAttributes->Color = clRed;
}
//---------------------------------------------------------------------------

void __fastcall TForm1::UpDown1Click(TObject *Sender, TUDBtnType Button)
{
          if ( ComboBox2->Text == "--" )  ;
          else
           {

      int fontsize = atoi(ComboBox2->Text.c_str());

    if(fontsize < 1)
     {
      ComboBox2->Text = 1;
     }
    else if(fontsize > 1638)
     {
      ComboBox2->Text = 1638;
     }

    RichEdit2->SelectAll();
    RichEdit2->SelAttributes->Size = StrToInt(ComboBox2->Text);
    RichEdit2->SelStart = 0;
           }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::ComboBox2Change(TObject *Sender)
{
    RichEdit2->SelectAll();
    RichEdit2->SelAttributes->Size = StrToInt(ComboBox2->Text);
    RichEdit2->SelStart = 0;
}
//---------------------------------------------------------------------------

void __fastcall TForm1::UpDown2Click(TObject *Sender, TUDBtnType Button)
{
          if ( ComboBox3->Text == "--" )  ;
          else
           {
    int fontsize = atoi(ComboBox3->Text.c_str());
    if(fontsize < 1)
     {
      ComboBox3->Text = 1;
     }
    else if(fontsize > 1638)
     {
      ComboBox3->Text = 1638;
     }

    RichEdit4->SelectAll();
    RichEdit4->SelAttributes->Size = StrToInt(ComboBox3->Text);
    RichEdit4->SelStart = 0;
           }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::ListBox1Click(TObject *Sender)
{
    Edit1->Text = ListBox1->Items->Strings[ListBox1->ItemIndex];

    RichEdit2->SelectAll();
    RichEdit2->SelAttributes->Name = Edit1->Text;
    RichEdit2->SelStart = 0;

    RichEdit3->SelectAll();
    RichEdit3->SelAttributes->Name = Edit1->Text;
    RichEdit3->SelStart = 0;

}
//---------------------------------------------------------------------------

void __fastcall TForm1::BitBtn2Click(TObject *Sender)
{
 FontDialog1->Options << fdApplyButton;
 if( FontDialog1->Execute())

    RichEdit3->Font = FontDialog1->Font;

    Edit1->Text = RichEdit3->Font->Name ;
    ComboBox2->Text = RichEdit3->Font->Size ;

    RichEdit2->SelectAll();
    RichEdit2->SelAttributes->Color = clBlack;
    RichEdit2->SelAttributes->Name = Edit1->Text;
    RichEdit2->SelAttributes->Size = StrToInt(ComboBox2->Text);

    RichEdit2->SelStart = 0;        
}
//---------------------------------------------------------------------------

void __fastcall TForm1::ComboBox3Change(TObject *Sender)
{
    RichEdit4->SelectAll();
    RichEdit4->SelAttributes->Size = StrToInt(ComboBox3->Text);
    RichEdit4->SelStart = 0;
}
//---------------------------------------------------------------------------

void __fastcall TForm1::RichEdit1MouseDown(TObject *Sender,
      TMouseButton Button, TShiftState Shift, int X, int Y)
{
      int poz, dl;
      if( Shift.Contains(ssDouble))
       {
               RichEdit4->Clear();      

            poz = RichEdit1->SelStart;
            dl =  RichEdit1->SelText.Length();

           RichEdit1->SelectAll();
           RichEdit1->SelAttributes->Color = clBlack;

           RichEdit1->SelStart = poz;
           RichEdit1->SelLength = dl;
           
               Edit2->Text = RichEdit1->SelText.Trim();
               RichEdit4->Text = RichEdit1->SelText.Trim();
               RichEdit4->SelectAll();
               RichEdit4->SelAttributes->Size = StrToInt(ComboBox3->Text);
               RichEdit4->SelAttributes->Name = Edit1->Text;
               RichEdit4->SelStart = 0;
               
           RichEdit1->SelAttributes->Color = clRed;

             RichEdit2->SelectAll();
             RichEdit2->SelAttributes->Color = clBlack;

             RichEdit2->SelStart = poz;
             RichEdit2->SelLength = dl;
             RichEdit2->SelAttributes->Color = clRed;

           RichEdit1->SelStart = poz;
       }
}
//---------------------------------------------------------------------------


