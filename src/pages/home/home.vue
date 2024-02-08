<template>
  <view class="commentchart">
    <view v-for="item in CommentList" :key="item.id" class="eachComment">
      <view class="title">【{{ item.categorize }}】{{ item.title }}</view>
      <view class="header">
        <image
          :src="item.useravatar"
          mode="scaleToFill"
          class="avatar"
        />
      <text class="name">{{ item.username }}</text>
      <text class="time">{{ item.time }}</text>
      </view>
      <view class="comment">{{ item.comment }}</view>
      <view class="footer">
        <text class="like">
          关注: {{ item.like }}
        </text>
        <text class="save">
          评论: {{ item.save }}
        </text>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data(){
    return {
      CommentList: [
        {
          id: 1,
          categorize: '讨论',
          title: "程序员最大的悲哀是什么？",
          useravatar: "/static/img/user.png",
          username: "admin",
          time: '2024-02-08 17:00:00',
          comment: "公司卸磨杀驴，项目开发完就把我裁了。领导觉得，换个便宜的新人来做维护更划算。但他不知道，因...",
          like: 300,
          save: 9999
        },
        {
          id: 2,
          categorize: '求助',
          title: "女生最想收到的什么礼物？",
          useravatar: "/static/img/user.png",
          username: "admin",
          time: '2024-02-08 17:00:00',
          comment: "作为一个在送礼物方面得到老婆连续多年认可的人，我必须答一下这个题。熟悉我的朋友都知道，过去...",
          like: 99,
          save: 9999
        },
        {
          id: 3,
          categorize: '求助',
          title: "有没有高格调的情人节礼物推荐？",
          useravatar: "/static/img/user.png",
          username: "admin",
          time: '2024-02-08 17:00:00',
          comment: "写在前面：选择什么样的礼物，才能更好的表达出心中的万千情谊，是一件十分具有技术含量的事情：不...",
          like: 3050,
          save: 9999
        },
        {
          id: 4,
          categorize: '讨论',
          title: "本科绩点会是无法洗白的污点吗？",
          useravatar: "/static/img/user.png",
          username: "admin",
          time: '2024-02-08 17:00:00',
          comment: "对于我来说，如果本科绩点太高（3.8+/4.0）才会成为无法洗白的污点，因为它会在后面的日子里一直提...",
          like: 1999,
          save: 9999
        },
        {
          id: 5,
          categorize: '讨论',
          title: "学计算机不打ACM就没有出路吗？",
          useravatar: "/static/img/user.png",
          username: "admin",
          time: '2024-02-08 17:00:00',
          comment: "我的看法，ACM的这些所谓的“锻炼xx能力、提高xx能力”什么的，就是一种成功学，就和我们说某某...",
          like: 5560,
          save: 9999
        },
      ]
    }
  }
}
</script>

<style scoped>
  .eachComment {
    margin: 20rpx auto;
    width: 700rpx;
    height: 250rpx;
    border-bottom: 1px solid rgba(0,0,0,0.1);
    padding: 10rpx 10rpx 10rpx 10rpx;
  }
  .eachComment .header {
    display: flex;
    align-items: center;
    vertical-align: middle;
  }
  .eachComment .title {
    font-weight: 500;
    font-size: 18px;
  }
  .eachComment image {
    width: 35rpx;
    height: 35rpx;
  }
  .eachComment .name, .eachComment .time{
    color: rgb(163, 163, 163);
    margin-left: 10rpx;
  }
  .eachComment .time{
    font-size: 14px;
  }
  .eachComment .comment {
    margin-top: 15rpx;
    overflow-wrap: break-word;
    color: rgb(163, 163, 163);
    font-size: 14px;
  }
  .eachComment .footer {
    margin-top: 15rpx;
    color: rgb(163, 163, 163);
    font-size: 14px;
  }
  .eachComment .footer .save {
    margin-left: 20rpx;
  }
</style>