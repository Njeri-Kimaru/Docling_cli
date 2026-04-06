## What is Docling ???
Docling is an open source document processing library that converts various document formats into structured outputs.
Docling plays an important part in the RAG pipeline.

## I'll be taking you through the process of parsing PDFs into structured formats.

### Step 1: Set up
- Create the project structure in your terminal;
```shell
mkdir docling_cli
cd docling_cli
```
- Create your virtual environment and activate it.
Fedora

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cknjzi2wulm9mu25uxqo.jpeg)
Windows 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/tnz0t11essq3r85h25cj.jpeg)

### Step 2: Installing docling
```shell
pip install docling
docling --version
```
Fedora

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/eo6017k3vs4q1wu9z37v.png)

Windows

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/i5svweubh26mvz8fx7tj.jpeg)

Check the docling's version

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6hppa0i1j03xet2e86hp.png)

### Step 3: Creating input and outputs folders
- create a folder called data where you will stored your desired pdfs.
- create a new folder and name it outputs
then inside the folders create new folders called; markdown outputs, html outputs and json outputs.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vp27bsfk0h0ttorb2jz0.png)

### step 4: Default options.
Start by running default options
Changes pdf format into markdown.
run;
```
docling your-pdf
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hlc53h8htczj4lt1wcv0.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mdg4754gdk8ngghcrvyt.png)


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/otjr3hiis9wydpimsjhd.png)

### Step 5: Changing the pdfs into html format
```shell
docling --to html *.pdf --output ~Documents/docling_cli/outputs/html_outputs
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/awuw0owsm19mlihrna2f.png)

### Step 6: Changing the pdfs into other formats
#### 1. Markdown
```
docling --to md *.pdf --output ~Documents/docling_cli/outputs/markdown_outputs
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3cnza6xffqqdv95omjjx.png)


#### 2. Json
```
docling --to json *.pdf --output ~Documents/docling_cli/outputs/json_outputs
```
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cuufwel6js9kkbczotrc.png)


#### 3. Plain text
```
docling --to text *.pdf --output ~Documents/docling_cli/outputs/plaintext_outputs
```
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/s3ev3jvnot3i3npct86t.png)


#### 4. yaml
```
docling --to yaml *.pdf --output ~Documents/docling_cli/outputs/yaml_outputs
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6ktwkgb0fux76efv5qoq.png)


#### 5. html_split_page
```
docling --to html_split_page *.pdf --output ~Documents/docling_cli/outputs/html_split_page_outputs
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zpdlazql3iyhglcapu23.png)


#### 6. DOCtags
```
docling --to doctags *.pdf --output ~Documents/docling_cli/outputs/doctags_outputs
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/w7nxa84d44bc91d4fuzm.png)


#### 7. vtt
```
docling --to vtt *.pdf --output ~Documents/docling_cli/outputs/vtt_outputs
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ugs093q1pyftsyvrp4q8.png)



### Step 7: Analyzing the result findings.
I used three types of pdfss;
one with tables, the other with text and images and the other had tables and paragraphs. Here are my key findings;
The default options turned the outputs into markdown 

#### 1. Pdf with tables
- In HTML, the rows and columns came out better than they were in the original pdf. 
- Markdown outputs were good too as it wrote the tables in markdown format without losing anything. 
- JSON was broke everything down into nested objects
- Plain text was good too but not as compared to markdown.

#### 2. Pdf with text and images
- HTML lost the color of the images.


#### 3. Pdf with tables and paragraphs
- Paragraphs in all formats came out nicely as texts.
