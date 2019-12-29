# Abaper
SAP

# Editor

  Notepad ++

  sourceforge.net

# Program Development

* Package 
  
  its attr includes Appl Components, Transport Layer, and Req no.

* Program

  its attr includes Title, "Type", Status, and Application.
 
* Class

* Code

  https://github.com/QueenieCplusplus/Abaper/blob/master/Hi.ABAP.rtf

* Text Message

___________________________

# Statement

. , end.

/ , write in alternative line.

: , chain statement.

＊ , comment.

___________________________

# Hot Key

F8 -> Execute

___________________________

# Help

execute T-code -> to ref to ABAPDOCU

___________________________

# Data Element Object

define Var

       KeyWord  var   options    type      val             options
          DATA  <f> [<length>]  <type>  [<initial value>] [<decimals>]
          
customed Var

       KeyWord  var   options    type      
          TYPES  <v> [<length>]  <type>  
     
  https://github.com/QueenieCplusplus/Abaper/blob/master/Data.ABAP.rtf
     
Type:

default space plz see https://noahchou.wordpress.com/2011/04/25/abap-範例程式：demonstrates-elementary-data-objects/

* C, char

* N, numerics

* I, integer

* D, date

* P, package#

* T, time

* F, float

* X, hexdial

___________________________

# Describe

  對 field 的存取方式
  
  範例：
  
        DESCRIBE FIELD var1 LENGTH vLen IN CHARACTER MODE.
        
        WRITE: var1, 'has length', vLen.
  
   https://noahchou.wordpress.com/2011/04/26/abap-範例程式：demonstration-of-describe-field/
___________________________

# Math Operations

* /

* DIV

* MOD

* ADD

* ＊＊

            ADD field1 THEN field2 UNTIL field6 GIVING sum.
>>>           

            ADD field1 THEN field2 UNTIL field6 GIVING sum.

MULTIPLY_CORRESPONDING，此用法現在已經廢除！ 

            MULTIPLY_CORRESPONDING field1 BY field2
            
___________________________

* String Process 

  TBD

* Math Function

  TBD

* Date & Time Calculation

  TBD

___________________________

#  Business Arithmetics

    TBD
___________________________

# Data Structure

  https://github.com/QueenieCplusplus/Abaper/blob/master/DataStructure.ABAP.rtf

             TYPES: BEGIN OF  <Structure Name>,
             
                            ,
                            
                            ,
                            
                            //...,
             
                    END OF <Structure Name>.
                    
              Write //...
              
MOVE-CORRESPONDING，兩結構的同樣變數給予相同賦值。

              MOVE var1 TO var2

  https://noahchou.wordpress.com/2011/04/25/abap-範例程式：demonstration-of-structures/

Internal Table https://noahchou.wordpress.com/2011/04/25/abap-範例程式：demonstration-of-internal-tables/

___________________________

# Data Class
  
  資料類別邏輯上定義了新增的 Table 儲存在 DB 的物理區域。
  
  
      TablesSpaceA    TableSpaceB   TableSpaceC     TableSpaceD     TMP
      Master          Company       Transaction     System          USER

      Table1               
      Table6          Table2        Table3          Table4
      Table8          Table7        Table5          Table9          Table

   其中，主資料幾乎不會被修改，而交易資料經常被修改，公司資料僅在系統安裝後自訂過程中定義一次。
   而其他資料類別，被稱為使用者，放置於特別儲存區，必須在資料庫中分配。
   
   https://github.com/QueenieCplusplus/Abaper/blob/master/Data_Class.png
___________________________

# ALV, ABAP List Viewer

  TBD
  
  https://noahchou.wordpress.com/2011/12/07/較多功能的alv範例/#more-2586

___________________________

# Buffer Setting

資料表設定緩衝，能夠讓資料表紀錄被讀取時，加快讀取速度，適用於經常被訪問，但很少被寫入的資料表。


                                    ABAP Program

                                        DBI
                     
                                       Network

                          DB -> DB Process <-> DB Buffer


