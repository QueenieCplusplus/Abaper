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

* D, data, 可以進行運算的字符類型

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

* String Process, 字串操作語句

  SKIP. 空一行
  
  ULINE. 畫線
  
  * Shift
  
  把字符串位按照各種方向移動指定長度，左移或回轉(把移出的字串長度的字符從另一方向回填)。
  把字符串按照各種方向移動道指定字符位置。
  移動時刪除指定字符串。

      SHIFT <c> [BY <n> PLACES] [<modes>]

      SHIFT {c} UP TO {str} {mode}.

      SHIFT {c} LEFT DELETING LEADING {C1}. 

      SHIFT {c} RIGHT DELETING TRAILING {C1}. 
  
  * Replace
  
  替換字串符
  
      REPLACE <string1> WITH <string2> into <C>.
  
  * Translate
  
  大小寫轉換
  
        TRANSLATE <c> TO UPPER CASE.

        TRANSLATE <c> TO LOWER CASE.
  
  * Overlay
  
  覆蓋字符字段 [限制字符]
  
      OVERLAY <c1> WITH <C2> [ONLY<str>]. 
      
  * Search
  
  查找字串符
  
       SEARCH {c} FOR {str} {options}.
       
  其中模式包含
  
  str
  
  .str
  
  *  +  str
  
  str + *
  
  https://noahchou.wordpress.com/2011/05/03/abap-範例程式：processing-strings/
  
  參數的指定
  
  STARTING AT {n1} 指定開始位置
  
  ENDING AT {n2} 指定結束位置
___________________________

* Math Function

  DATA n TYPE p DECIMALS 2.
  
  DATA m TYPE p DECIMAL2 VALUES '-9.99'

  abs(). 絕對值
  
  exp(). 指數
  
  log(). 對數
  
  log10(). 底數為10的對數
  
  sign(). 返回參數的符號(或稱字符)
  
  trunc(). 返回參數的整數部分
  
  frac(). 返回參數的小數部分
  
  ceil(). 返回不小於參數的最小整數
  
  floor(). 返回不大於參數的最小整數
  
___________________________

* Date & Time Calculation


        DATA: ultimo TYPE d.
        
        ultimo = sy-datum.
        
        WRITE ultimo.

  Costant:
  
  *SPACE
  
  *SY-SUBRC, 系統執行傳回值
  
  *SY-UNAME logon, 帳號
  
  *SY_DATUM, 系統日期
  
  *SY_UZEIT, 系統時間
  
  *SY-TCODE, 目前交易的代號
  
  https://github.com/QueenieCplusplus/Abaper/blob/master/Date_Conversion.ABAP.rtf
___________________________ 

# Message Maintenance, 彈出訊息

由點選 Goto 按鈕進入，新增此警示訊息，進入 Message 頁籤，內部有定義訊息的 4 個參數，如要使用
長字串，則不能選擇 self-explanatory。

訊息類型：

* E, error

* W, warn

* I, info

* A, abnormal

* S, success

程式碼撰寫完畢後，點選啟用與執行。

      REPORT PQK_TEST_MSG.
      
      MESSAGE ID 'PQK' TYPE 'E' NUMBER '003'.
___________________________

#  Business Arithmetics, 商業邏輯運算

     REPORT QsBizReport
     
     DATA bottle TYPE p DECIMALS 0.
     
     bottle = 1 / 12.
     
     WRITE bottle.
     
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

  定義步驟：
  
 （1）定義SLIS，使用Layout和Fieldcat前需進行宣告。
  
  (2) 定義FIELDCAT 和 LAYOUT。
   
  (3) 定義程式中所要使用的資料表。

  (4) 利用透明表 Form GETDATA 讀取資料。
   
  (5) 表皮輸出：

  https://github.com/QueenieCplusplus/Abaper/blob/master/FormALV_Show.ABAP.rtf
  
  相關連結：
  
  https://noahchou.wordpress.com/2011/12/01/簡單的alv範圍/
  
  https://noahchou.wordpress.com/2011/12/07/較多功能的alv範例/#more-2586

___________________________

# Buffer Setting

資料表設定緩衝，能夠讓資料表紀錄被讀取時，加快讀取速度，適用於經常被訪問，但很少被寫入的資料表。


                                    ABAP Program

                                        DBI
                     
                                       Network

   
                             DB -> DB Process <-> DB Buffer
                             
                             
___________________________

# Basis

https://noahchou.wordpress.com/sap-basis模組設定手冊/
