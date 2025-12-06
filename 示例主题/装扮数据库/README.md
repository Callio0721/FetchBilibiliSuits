解释一下skin.db  
来源于 https://github.com/Rovniced/bilibili-skin 和之后上传到Telegram频道 https://t.me/Bilibili_skin 中的哔哩哔哩个性装扮  
于2025年1月1日上传到Telegram中

发布原文如下:  
以下为哔哩哔哩装扮的数据（除了极少数已经下架的，基本都有）
（有部分name字段为空的就是之前已经下架的套装）

skin table为套装
act table为收藏集（收藏集数据不完整，后面需要改成卡池数据）

字段解释：
item_id：装扮ID
item_name：装扮名称
msg_id：消息id，对应 https://t.me/Bilibili_skin/消息ID
sticker_id：https://t.me/addstickers/贴纸ID
type：装扮类型
data：原始数据
file_id：tg bot发送出去的id，这个字段不需要管
```python
class SkinType(Enum):
    """装扮类型"""
    act = 0  # 收藏集（自定义的）
    avatar = 1  # 头像
    card = 2  # 动态卡片
    thumb = 3  # 点赞
    emoji = 4  # 单个表情
    emoji_package = 5  # 表情包
    suit = 6  # 套装
    space_bg = 7  # 背景
    pendant = 8  # 头像
    skin = 9  # 装扮
    loading = 10  # 加载动画
    play_icon = 11  # 进度条
```
