import streamlit as st
from PIL import Image

st.set_page_config(page_title='图片无损放大', page_icon=':camera:')

st.title('图片无损放大')

ratio = st.slider('放大倍数', 1, 10, 3) 

uploaded_file = st.file_uploader('上传图片', type=['jpg', 'png', 'jpeg'])

if uploaded_file is not None:
    img = Image.open(uploaded_file)
    w, h = img.size

    new_w = w * ratio
    new_h = h * ratio

    new_img = Image.new('RGB', (new_w, new_h))
    new_img.paste(img, (0, 0, w, h))

    st.image(new_img, caption='放大后的图片')

else:
    st.write('请上传图片文件') 
