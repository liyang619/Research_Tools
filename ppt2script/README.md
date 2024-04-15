# Auto Generate Speech Script From PPT - Based on ChatGPT

### Yang forks and refines the repo from "https://github.com/VITA-Group/ppt2script"... Thanks Wenqing Zheng. 

This repository helps to generate speech with "1-click". Leveraging the power of ChatGPT, it read the layout and content of your slides, and synthesis the speech text.

Watch this [video](https://www.youtube.com/watch?v=RQkCXz2nDyQ) (no sound) for a quick demo. 

# How to use it? 
First, you need to place your powerpoint file in the folder and modify the path (or just point to where you place your ppt).

Then you need to give a abstract and replace the demo context in abs.txt. 

Also you could modify the save_path, and the max generated sentences for on page.

```python
    pptx_path = 'demo.pptx'
    abs_file = 'abs.txt'
    save_path = 'results'
    sentence_cnt = 10  
```

Besides, you need to fillin your openai key:
```python
    openai.api_key = 'your-api-key'
```
and set the use_paid_API as True to call the API. 
```python
    auto_summary_ppt(abs_file, save_path,sentence_cnt,use_paid_API=False)
```

At last, just run the command to generate the script, which will be saved in "{save_path}/chatGPT_API_result.txt".
```code
python ppt_script_gen.py
```

# Requirements
```code
pip install -r requirements.txt
```

