![image](https://github.com/darkhoundz/KLCiS-AdoPisoft-E-Payment/assets/28075740/5854f4c9-b522-4ff4-af5f-aa70aa07640a)

**KLCiS Voucher System** supports all AdoPisoft versions whether it is Lite or Business license.

**REQUIREMENTS:** <br><br>

1. KLCiS Voucher System account and API Key. Signup: ` https://s2.klinternetservices.com/ ` <br>
2. Download the KLCiS AdoPisoft v5.1.4 Embedded Theme: [KLCiS_AdoPisoft_v5.1.4_Theme_Embedded.zip](https://github.com/darkhoundz/KLCiS-AdoPisoft-E-Payment/blob/master/KLCiS_AdoPisoft_v5.1.4_Theme_Embedded.zip) <br
3. Voucher codes to be imported to KLCiS Admin Panel.
4. Watch this tutorial on how to edit the CSV file and how to import it your KLCiS Dashboard: [https://www.youtube.com/watch?v=xpGXiQRlirY](https://www.youtube.com/watch?v=xpGXiQRlirY) <br><br>


**INSTRUCTIONS:**

1. Backup your current theme, on your AdoPisoft admin panel, go to: ` http://10.0.0.1/admin#!/theme/variants ` and download your active theme.
2. On the same page, click the Upload button and upload the KLCiS AdoPisoft theme.
3. Next, Go to Code Editor, ` http://10.0.0.1/admin#!/theme/code-editor ` and search for the **home-page.html**
4. Find and edit these lines:
   
       <select class="form-control" id="amountDropdown" name="amount" style="font-size:16px; font-weight:500; color:green;">
       <option value="11">₱11.00 - PROMO! 1 DAY UNLI (no pause)</option>
          <option value="5">₱5.00 - 4 HOURS (no exp.|unli pause)</option>
              <option value="10">₱10.00 - 10 HOURS (no exp.|unli pause)</option>
              <option value="20">₱20.00 - 1 day (no exp.|unli pause)</option>
              <option value="50">₱50.00 - 3 DAYS INTERNET</option>
              <option value="100">₱100.00 - 7 DAYS INTERNET</option>
            <option value="180">₱180.00 - 15 DAYS INTERNET</option>
            <option value="300">₱300.00 - 30 DAYS INTERNET</option>
       </select>
   
   Make sure that the **value=""** inside matches the amount/price of the voucher which you have uploaded in the KLCiS dashboard.
   
6. Then, find this line and add your KLCIS API Key.

       <input type="hidden" class="form-control" id="tokenInput" name="token" value="YOUR_API_KEY_HERE">

8. Congratulations on your embedded voucher store 🙂
