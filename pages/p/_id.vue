<template>
    <div @click="closeshow">
        <my-header></my-header>
        <div class="note">
            <!--文章区域-->
            <div class="post">
                <!--正文-->
                <div class="article">
                    <h1 class="title">月薪三千，就该去死吗？</h1>
                    <div class="author">
                        <nuxt-link to="/u/123" class="avatar">
                            <img src="../../assets/img/default-avatar.jpg">
                        </nuxt-link>
                        <div class="info">
                            <span class="name">测试用户</span>
                            <a href="javascript:void(0)" class="btn-sm follow" v-if="isShow" @click="isFollow">
                                <i class="fa fa-plus-square-o"></i>
                                关注
                            </a>
                            <a href="javascript:void(0)" class="btn-sm follow follows" v-if="!isShow" @click="isFollow" @mouseenter="Follow=false" @mouseleave="Follow=true">
                                <span v-show="Follow">
                                    <i class="fa fa-check"></i>
                                    已关注
                                </span>
                                <span v-show="!Follow">
                                    <i class="fa fa-close"></i>
                                    取消关注
                                </span>
                            </a>
                            <div class="meta">
                                <span>2018.01.23 16:09</span>
                                <span>字数 2273</span>
                                <span>阅读 882</span>
                                <span>评论 7</span>
                                <span>喜欢 34</span>
                            </div>
                        </div>
                    </div>
                    <div class="show-content">
                        <p>可能是春节快要到了，游子回家的旋律吹响，一年一度的“比头疼大赛”又要拉开大幕。
                            比什么？比工作，比资产，比儿女，比婚姻。都市人携带着远方不为所知的辛苦，
                            在同学相聚时，多了些虚伪；在朋友重逢时，少了些真诚。</p>
                        <p>家乡是个让人又爱又恨的地方。有时，常看见有人自嘲：在外大老板，回乡二胖子；
                            在外大哥大，回镇三孙子；在外大名媛，回村小豆子；
                            在外喜当爹，回家好多爹——亲爹不倒，干爹飘飘。</p>
                        <p>上周末，一众平台大号撰稿了类似“过年回家让你最害怕的事”这样一个主题。
                            与往年千篇一律的抱怨答案不同，今年出来的评论里更多年轻人是对自己能力桎梏、工资不高的恐慌。
                            当年的小愤青们长大，逐渐意识到生活的困境，其实这是一种成长。
                            但是“爱搞事”的公众号另辟蹊径，就像《演员的诞生》节目会鬼魅剪辑一样，
                            平台大编辑整合评论后，推出来一篇“工资三千的男人值不值得嫁”这样一个帖子，
                            成功点燃新一轮的社会讨论。</p>
                        <p>没办法，中国女性地位早已不是“重男轻女”的时代，
                        代表着女权主义的评论清一色地给出“不能嫁”的结论，并嘲讽地说：“老娘自己都能赚到这个数，
                        还要你这老爷们何用？”
                        此等答案有几千人点赞，于是“代表底层大众”的“月薪三千的男人”被拉出来各种声讨。</p>
                        <p>先别忙着歧视，也别忙着诉苦，我们先来讲两个类似的故事。</p>
                        <hr>
                        <p>1.</p>
                        <p>我一高中同学，是河北某三线城市的，在工厂当技术员。当地人均工资不到两千，而他月薪三千的收入，
                            足够他生活所需。</p>
                        <p>并且他这个人也足够“佛系”，很早地就把生活定位在“快乐就好”的基调上。 前年他结婚时，
                            我去参加了婚礼，现场别的花样没有，就只见到他和他老婆两个人在整场典礼上都发出傻笑的画面。
                            这还不算，双方的父母也都是“两排牙齿一起亮”的节奏，整个一“中国好笑容”。
                            我和一起同来的高中老班长面面相觑，很久之后他自言自语道：“他们脑袋是不是都瓦特了？”</p>
                        <p>不过让我感动的是，同学老婆虽然是大学毕业思想独立的知识女性，但依旧保持着爱情的初心，
                            两家没有彩礼往来，女方给予了我同学心里满满的依赖和眼里满满的爱意。</p>
                        <p>同学告诉我，两人达成一致，生活以满足基本要求就好，在能力范围内享受奢侈。
                            女方月工资两千五，两人在双方家里的帮助下买了一个小房，装修得相对小资，
                            在那个城市里活得很滋润。</p>
                        <p>我们的班长还是对他没选择一线城市奋斗表示惋惜， 甚至为他儿女将来面临的竞争问题表示担心。
                            但是他不奢望他的孩子一定要考上多么重点的学校，获得多么成功的人生；
                            而且他觉得他的生活里孩子只是一小部分，他和他老婆还有自己的人生追求。</p>
                        <p>后来我们参加完婚礼就赶紧走了，两人实在是甜得发齁，让我们鸡皮疙瘩三尺高，难受。</p>
                        <p>去年他们有了孩子，生活并没有像我们班长当时说的“有了孩子你们就有矛盾”那般残酷。
                            这几年来，我十分想屏蔽他天天晒老婆的“尬笑”朋友圈，但是我的仁慈打败了我的理智。
                            今天我问他关于“月薪三千的男人”这个话题时，他第一句回复是赤裸裸的撒狗粮：
                            “不是每个男人都能碰见我老婆这么好的女孩子。”第二句则是恶狠狠地为自己正名：
                            “老子工资是三千零五十块七毛八，不是你们那个档次的！”</p>
                        <hr>
                        <p>2.</p>
                        <p>我大学的一个好哥们，毕业后考了公务员，抱上了铁饭碗，我们很是羡慕他——当然不是羡慕他的工作，
                            而是他的女朋友，那叫一个漂亮，那叫一个带劲。</p>
                        <p>但是在他当上公务员的第二年，他们就分手了，原因很直接：他一个月的工资，
                            都够不上女朋友那一套lamer面霜。彼时他拿到手的钱和各种单位福利正好在三千多一点，
                            符合我们这篇稿子探讨的要求。</p>
                        <p>我哥们沉寂了一阵，但对工作兢兢业业，从不马虎。 没想到他得到了一个表现的机会，
                            他的文笔和口才被领导相中，调到了更高级别，工资涨了一千 ， 然后今年，
                            已经达到了五千的水平。</p>
                    </div>
                    <div class="show-footer">
                        <nuxt-link to="/nb/123" class="notebook">
                            <i class="fa fa-file-text-o"></i>
                            <span>我的文集</span>
                            <div class="copyright">
                                © 著作权归作者所有
                            </div>
                        </nuxt-link>
                    </div>
                    <div class="follow-detail">
                        <div class="info">
                            <nuxt-link to="/u/123" class="avatar">
                                <img src="../../assets/img/default-avatar.jpg" alt="">
                            </nuxt-link>
                            <a href="javascript:void()" class="btn btn-success">
                                <i class="fa fa-plus-square-o"></i>
                                关注
                            </a>
                            <nuxt-link to="/u/123" class="title">
                                测试用户
                            </nuxt-link>
                            <i class="fa fa-mars"></i>
                            <p>
                                写了 46873 字，被 26 人关注，获得了 95 个喜欢
                            </p>
                            <div class="signature">
                                为城市里的不安和孤寂发声。 微信公众号：得及
                            </div>
                        </div>
                    </div>
                    <div class="meta-bottom">
                        <div class="like">
                            <div class="btn like-group" @click="addOrMius" v-bind:class="{'color-a':isA,'color-b':!isA}">
                                <div class="btn-like">
                                    <a href="javascript:void ()" v-bind:class="{'color-c':isA}">
                                        <i class="fa fa-heart"></i>
                                        <span>喜欢</span>
                                    </a>
                                </div>
                                <div class="modal-wrap" v-bind:class="{'color-d':isA}">
                                    <a>{{msg.num}}</a>
                                </div>
                            </div>
                        </div>
                        <div class="share-group">
                            <a href="javascript:void ()" v-b-tooltip.hover title="分享到微博">
                                <i class="fa fa-weibo weibo"></i>
                            </a>
                            <a href="javascript:void ()" v-b-tooltip.hover title="分享到微信">
                                <i class="fa fa-weixin weixin"></i>
                            </a>
                            <a href="javascript:void ()" v-b-tooltip.hover title="分享到QQ">
                                <i class="fa fa-qq qq"></i>
                            </a>
                            <a href="javascript:void ()" class="more-share" @click="openshow">
                                更多分享
                                <ul class="share-list" v-if="moreshow">
                                    <li>
                                        <i class="fa fa-star list-qq"></i>
                                        <span>分享到QQ空间</span>
                                    </li>
                                    <li>
                                        <i class="fa fa-twitter list-twitter"></i>
                                        <span>分享到Twitter</span>
                                    </li>
                                    <li>
                                        <i class="fa fa-facebook-square list-facebook"></i>
                                        <span>分享到FaceBook</span>
                                    </li>
                                    <li>
                                        <i class="fa fa-google-plus list-google"></i>
                                        <span>分享到Google</span>
                                    </li>
                                </ul>
                            </a>
                        </div>
                    </div>
                </div>
                <!--回复组件-->
                <my-comment></my-comment>
            </div>
            <!--悬浮的操作框-->
            <div class="side-bar"></div>
            <!--对应的推荐阅读-->
            <div class="note-bottom"></div>
        </div>
    </div>
</template>

<script>
  import  myHeader from '~/components/myHeader'
  import myComment from '~/components/myComment'
  export default {
    name: "_id",
    data(){
      return {
        isShow:true,
        Follow:true,
        moreshow:false,
        msg:{
          num:56,
          flag:true
        }
      }
    },
    components:{
      myHeader,
      myComment
    },
    methods:{
      isFollow(){
        this.isShow=!this.isShow;
      },
      closeshow(){
        this.moreshow = false
      },
      openshow(){
        this.moreshow = true
        event.stopPropagation()
      },
      addOrMius() {
        this.msg.num = this.msg.flag ? this.msg.num + 1 : this.msg.num - 1 ;
        this.msg.flag = !this.msg.flag;
        this.isA = !this.isA;
      }
    }
  }
</script>

<style scoped>

</style>
