//onMeasure模板
```
protected void onMeasure(int widthMeasureSpec,int heightMeasureSpec){
    super.onMeasure(widhtMeasureSpec,heightMeasureSpec);
    
    int widthMode = MeasureSpec.getMode(widthMeasureSpec);
    int widthSize = MeasureSpec.getSize(widthMeasureSpec);
    
    int resultWidth=500;
    if (widthMode == MeasureSpec.AT_MOST){
        resultWidth = Math.min(resultWidth,widthSize);
    }else if(widthMode == MeasureSpec.EXACTLY){
        resultWidth = widthSize;
    }
    
    int heightMode =MeasureSpec.getMode(heightMeasureSpec);
    int heightSize =MeasureSpec.getSize(heightMeasureSpec);

    int resultHeight =500;
    if (heightMode == MeasureSpec.AT_MOST){
        resultHeight=Math.min(resultHeight,heightSize);
    }else if (heightMode == MeasureSpec.EXACTLY){
        resultHeight= heightSize;
    }

    setMeasuredDimension(resultWidth,resultHeight);
}
```

//一张图看懂android坐标系<br>
![一张图看懂android坐标系](https://github.com/twangithub/TwanLib/blob/master/assets/%E8%A7%86%E5%9B%BE%E5%9D%90%E6%A0%87%E7%B3%BB.png)
