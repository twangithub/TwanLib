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
![Alt text](![Alt text](/path/to/img.jpg))
