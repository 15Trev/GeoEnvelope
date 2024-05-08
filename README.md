# GeoEnvelope - A Maps-to-Mail App
Please read this full README first

![Demo Image](https://github.com/15Trev/GeoEnvelope/blob/main/GeoEnvelope_demo.png)

The map will not display until you follow the steps to set up your API key:

1) Go to the Google Cloud Console: Navigate to the Google Cloud Console at https://console.cloud.google.com/ and create an account or login to start the API key setup.
	
2) Select Your Project: If you have multiple projects, make sure you have selected the correct project from the project selector at the top of the page.

3) In the Cloud Console, navigate to the "APIs & Services" > "Library" section. Search and enable each: <br>
-Maps JavaScript API <br>
-Geocoding API <br>
-Places API

4) Create or Update API Key: Go to "APIs & Services" > "Credentials" and create a new API key or use an existing one. Make sure the API key is associated with your project.

5) Replace API Key: Replace the placeholder 'YOUR_API_KEY' on line 504 in the GeoEnvelope.html file with your actual API key.

Once you have enabled all 3 APIs and updated your API key, reload your web page. The error should no longer occur, and the map should load properly. If you continue to encounter issues, double-check that the API key is correctly configured and associated with the project.<br>

To add a custom address header: Remove the "`<!--`" and "`\-->`" from "`<!--ADDRESS_HEADER_LINE_HERE<br>-->`" on line 438 and update the "ADDRESS_HEADER_LINE_HERE" accordingly.

Additional Note:<br>
All of the addresses are populated in #10 envelope formatting. Adjust for different envelope sizes and printer dimensions accordingly. I had to define the print setup page to Orientation = Landscape, Paper size = Envelope #10, Scale = 100 (Scale = 99 on Firefox), Margins = None. To try with different envelope sizes, try editing the width and height dimensions on lines 441 & 442 to the new envelopes' pixel size equivelent. Example:<br>
Height: 4.125 inches × 96 pixels/inch = 396px (4px padding added for browser inconsistnecies to = 400px)<br>
Width: 9.5 inches × 96 pixels/inch = 912px

*Reconfigure as needed*

-------------------------------------------------------------

Freedom Flyer in Google Sheets: https://docs.google.com/spreadsheets/d/1Tlpk8AtPhpYeOiJ6p_30CW3YdZ1zHDzKXTtnnp8oxUM/edit?usp=sharing <br>
The official "Freedom_Flyer_Sharable_Template.ods" is accessable as a free excel file by downloading and installing LibreOffice Calc:
https://www.libreoffice.org/download/download-libreoffice/