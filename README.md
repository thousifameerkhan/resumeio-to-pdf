# Resume.io to PDF

***
Changes - Nov 24
Author : Thousif Ameer Khan

Modifed the Docker composer file. 
The Dependencies during the installation were failing.
I have corrected the env variables

***

How to Use it.
By clicking the Download button, You will see the some content in the browser, 
You have to save the Content by clicking ctrl+s and changing the extension as .pdf

Important point : 
The download is not immediate, You have to wait for few mins for the download to complete

***
Observation :
The tool does not seem to work in the latest Google chrome.
The problem faced is that if we try to save the contents on the webpage, the files takes some time to Download. Meanwhile the Google chrome browser is removing it.

I have used Microsoft Edge and repeated the same process. it saved correctly.

***


Download your resume from [resume.io](https://resume.io) as a PDF file. 

<div align="center"><a href="https://resumeio-to-pdf.fly.dev/"><img src="https://github.com/felipeall/resumeio-to-pdf/assets/20917430/b7edfda4-4768-4659-af68-561e1effe628" width="700" /></a></div>

Open the application, enter your resume `renderingToken` and click the download button. 
It will automatically download your resume as image files, merge them, inject the hyperlinks,
convert to a PDF file and run OCR to extract the text.

### How to find your renderingToken

Go to https://resume.io/api/app/resumes

You will see a list of your resumes. Find the one you want to download and get the `renderingToken` from 
the payload.

### How to run the application

Clone the repository
```bash
git clone https://github.com/felipeall/resumeio-to-pdf.git
```
    
Go to the project's root folder
```bash
cd resumeio-to-pdf
```

Build the image
```bash
docker build -t resumeio-to-pdf .
```

Run the container
```bash
docker run -p 8000:8000 resumeio-to-pdf
```

Open your browser and access http://localhost:8000

### Disclaimer

Please be advised that this application is designed for preview purposes only. 

By utilizing this tool, you explicitly agree to adhere to all applicable laws and regulations governing the use of such services. 
The creators of this application absolve themselves of any responsibility for potential damages or harm resulting from its utilization.

It is essential to visit the pricing page on Resume.io to explore fair and affordable options for accessing the resume downloading service directly through the official channels provided by Resume.io. 
The creators emphasize the importance of supporting the platform by subscribing to their services and discourage the use of this application as a substitute for legitimate and paid access.
