# music-player
## 项目介绍：
- 业务功能：本项目是仿QQ音乐的移动端音乐播放应用，核心业务（页面）包括：【推荐页面】、【歌手页面】、【歌手详情页面】、【播放器页面】、【歌单页面】、【排行榜页面】、【榜单列表页】、【搜索页面】、【歌曲列表页】、【用户中心页】
- 开发目的：本项目属于个人项目，主要用于学习Vue.js 和熟悉移动端开发，因为具备一定的AngularJS4的基础，对组件化开发有一定经验，所以想直接通过上手项目来学习Vue.js组件化开发，这个项目也基本包含了很多实际开发工作中的业务逻辑。
- 开发工具：前端核心框架使用vue.js，后台数据均从QQ音乐调取</br>
【基础组件库】：better-scroll、vue-lazyload等</br>
【状态管理】：vuex</br>
【路由】：vue-router</br>
【服务端通讯】：axios & jsonp</br>
【脚手架工具】：vue-cli</br>
【自动化构建】：webpack</br>
【代码检查】：eslint</br>
- 项目运行：
1. npm install
2. npm run dev
3. 访问 http://localhost:8080
## 当前进度：
推荐（首页）、歌手页、歌手详情页初步完成
## 代码逻辑：
- 核心目录结构：</br>
【api文件夹】：数据接口相关，数据主要抓取自QQ音乐</br>
【base文件夹】：重用性较高的基础组件相关</br>
【common文件夹】：公共资源，包括字体、图片、重用方法、重用样式等</br>
【components文件夹】：核心业务组件相关</br>
【controllers文件夹】：核心业务对应的数据初步处理相关</br>
【router文件夹】：路由相关</br>
【store文件夹】：vuex状态管理相关</br>
- 组件介绍（已完成部分）：</br>
【scroll】:基础组件。better-scroll组件的初步封装，用于滚动场景</br>
【slider】：基础组件。用于轮播，主要根据传入数据设置容器宽度，并处理轮播基础逻辑</br>
【loading】：基础组件。数据未加载完成时显示提示信息</br>
【listview】：基础组件。主要用于分组数据的显示，包括分组导航和分组数据，二者在列表滚动时实现联动。如在歌手列表中，歌手以姓名首字母分类，则组件渲染出所有首字母组成的锚点列表和歌手组成的数据列表，在数据列表滚动时监听滚动事件，计算当前数据所在的分组，将其标题固定显示，并让对应的锚点高亮。同样在锚点列表中监听相关触摸事件计算当前触摸抵达的目标锚点，控制数据列表联动滚动。</br>
【songlist】：基础组件。歌曲列表封装</br>
【main-header】：业务组件。header部分</br>
【main-nav】：业务组件。导航部分</br>
【recommend】：业务组件。推荐页面。包括热门的推荐的slider轮播和推荐歌单列表</br>
【singer】：歌手列表。按姓名首字母排序。点击歌手跳转到歌手详情。</br>
【singer-detail】：【singer】组件中的子路由。显示歌手歌曲等信息。</br>
