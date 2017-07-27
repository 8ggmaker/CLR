1. Primitive Type

   - Primitive Type vs FCL Type

     | Primitive Type | FCL Type (Framework Class Library) |
     | :------------: | :--------------------------------: |
     |     sbyte      |            System.SByte            |
     |      byte      |            System.Byte             |
     |     short      |            System.Int16            |
     |     ushort     |             System.UIn             |
     |      int       |            System.Int32            |
     |      uint      |           System.UInt32            |
     |      long      |            System.Int64            |
     |     ulong      |            System.UInt             |
     |      char      |            System.Char             |
     |     float      |           System.Single            |
     |     double     |           System.Double            |
     |      bool      |           System.Boolean           |
     |    decimal     |           System.Decimal           |
     |     string     |           System.String            |
     |     object     |           System.Object            |
     |    dynamic     |           System.Object            |


   - Checked and Unchecked Primitive Type Operations

     checked for IL instructions: *add.ovf*, *sub.ovf*, *mul.ovf*, *conv.ovf* which include *OverflowException* checking.

     unchecked for IL instructions: *add*, *sub*, *mul*, *conv* with no checking

     ```c#
     checked{
       CastInt32ToByte(400);
     }
     // this code may throw OverflowException or not, it depends on // how method CastInt32ToByte is compiled, because checked 
     // operator and statement only affects which version of add,  // subtract, multiple and data conversation IL instructions are // generated
     ```

     ​

     ​