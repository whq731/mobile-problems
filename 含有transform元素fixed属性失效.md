足球游戏中遇到

After some research, there has been a bug report  on the Chromium  website about this issue, so far Webkit browsers can't render these two effects together at the same time.
I would suggest adding some Webkit only CSS into your stylesheet and making the transformed div an image and using it as the background.
        @media screen and (-webkit-min-device-pixel-ratio:0) {
            /* Webkit-specific CSS here (Chrome and Safari)*/
#transformed_div {
    styles here, background image etc }
}
So for now you'll have to do it the old fashioned way, until Webkit browsers catch up to FF.
EDIT: As of 10/24/2012 the bug has not been resolved.

http://stackoverflow.com/questions/2637058/positions-fixed-doesnt-work-when-using-webkit-transform


解决：
去掉transform 