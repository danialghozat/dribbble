<template>
  <ol class="cardsBox">
    <li class="card" v-for="(post ,index) of posts" :key="index">
        <div class="cardPic" :style="{backgroundImage: `url(${post.cover})`}" >
          <div class="hoverTime">
            <div class="postName">{{post.title}}</div>
            <div class="postSituation">
              <div class="addToFile">
                <svg xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" viewBox="0 0 24 24" role="img" class="icon "><path d="m22 5h-11l-2-3h-7c-1.104 0-2 .896-2 2v16c0 1.104.896 2 2 2h20c1.104 0 2-.896 2-2v-13c0-1.104-.896-2-2-2zm-6 10h-3v3c0 .55-.45 1-1 1s-1-.45-1-1v-3h-3c-.55 0-1-.45-1-1s.45-1 1-1h3v-3c0-.55.45-1 1-1s1 .45 1 1v3h3c.55 0 1 .45 1 1s-.45 1-1 1z"></path>
                </svg>
              </div>
              <div class="likeButton">
                <svg xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" viewBox="0 0 24 24" role="img" class="icon "><path d="m18.199 2.04c-2.606-.284-4.262.961-6.199 3.008-2.045-2.047-3.593-3.292-6.199-3.008-3.544.388-6.321 4.43-5.718 7.96.966 5.659 5.944 9 11.917 12 5.973-3 10.951-6.341 11.917-12 .603-3.53-2.174-7.572-5.718-7.96z"></path>
                </svg>
              </div>
            </div>
          </div>
        </div>
        <div class="user">
          <div class="userInfo">
            <div class="userPic">
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:svgjs="http://svgjs.com/svgjs" version="1.1" x="0" y="0" viewBox="0 0 512 512" style="enable-background:new 0 0 512 512" xml:space="preserve" class=""><g><path xmlns="http://www.w3.org/2000/svg" d="m463.09375 406.492188c31.71875-43.519532 48.90625-95.886719 48.90625-150.503907 0-141.480469-114.496094-255.988281-256-255.988281-141.488281 0-256 114.492188-256 255.988281 0 54.601563 17.179688 106.953125 48.878906 150.464844 102.132813-140.484375 311.9375-140.609375 414.214844.039063zm-297.09375-255.5c0-49.621094 40.375-89.996094 90-89.996094s90 40.375 90 89.996094v30c0 49.625-40.375 89.996093-90 89.996093s-90-40.371093-90-89.996093zm0 0" fill="#ea4c89" data-original="#000000" style="" class=""/><path xmlns="http://www.w3.org/2000/svg" d="m256 240.988281c33.085938 0 60-26.914062 60-59.996093v-30c0-33.082032-26.914062-59.996094-60-59.996094s-60 26.914062-60 59.996094v30c0 33.082031 26.914062 59.996093 60 59.996093zm0 0" fill="#ea4c89" data-original="#000000" style="" class=""/><path xmlns="http://www.w3.org/2000/svg" d="m68.757812 430.527344c101.289063 108.601562 273.167969 108.683594 374.550782-.074219-89.375-132.792969-284.695313-132.1875-374.550782.074219zm0 0" fill="#ea4c89" data-original="#000000" style="" class=""/></g>
              </svg>
            </div>
            <div class="userName">{{post.user.name}}</div>
            <div class="userType">{{post.user.type}}</div>
          </div>
          <div class="postInfo">
            <div class="like">
              <svg xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" viewBox="0 0 24 24" role="img" class="icon fill-current shot-tools-icon"><path d="m18.199 2.04c-2.606-.284-4.262.961-6.199 3.008-2.045-2.047-3.593-3.292-6.199-3.008-3.544.388-6.321 4.43-5.718 7.96.966 5.659 5.944 9 11.917 12 5.973-3 10.951-6.341 11.917-12 .603-3.53-2.174-7.572-5.718-7.96z"></path>
              </svg>
              <span>{{post.postLikes}}</span>
            </div>
            <div class="view">
              <svg xmlns="http://www.w3.org/2000/svg" width="14" height="11" viewBox="0 0 14 11" fill="none" role="img" class="icon fill-current shot-tools-icon">
                <path d="M7 3.45833C5.87242 3.45833 4.95833 4.37242 4.95833 5.5C4.95833 6.62758 5.87242 7.54167 7 7.54167C8.12758 7.54167 9.04167 6.62758 9.04167 5.5C9.04167 4.37242 8.12758 3.45833 7 3.45833ZM7 0.25C3.13425 0.25 0 4.625 0 5.5C0 6.375 3.13425 10.75 7 10.75C10.8657 10.75 14 6.375 14 5.5C14 4.625 10.8657 0.25 7 0.25ZM7 8.70833C5.22783 8.70833 3.79167 7.27217 3.79167 5.5C3.79167 3.72783 5.22783 2.29167 7 2.29167C8.77217 2.29167 10.2083 3.72783 10.2083 5.5C10.2083 7.27217 8.77217 8.70833 7 8.70833Z"></path>
              </svg>
              <span>{{post.postViews}}</span>
            </div>
          </div>
        </div>
    </li>
  </ol>
</template>

<script>
export default {
  name: "Cards",
  data (){
    return {
      posts : [
        {title: 'Web Design 1',postLikes :200 , cover : 'https://picsum.photos/315/220?random', postViews :1.23 + 'k' , user: {name : 'Danial' , type : 'PRO'}},
        {title: 'Web Design 2',postLikes :500, cover : 'https://picsum.photos/315/220?random=2'  , postViews :1.2 + 'k' , user: {name : 'Reza' , type : 'TEAM'}},
        {title: 'Web Design 3',postLikes :123 , cover : 'https://picsum.photos/315/220?random=5' , postViews :50 + 'k' , user: {name : 'John' , type : 'PRO'}},
        {title: 'Web Design 4',postLikes :145 , cover : 'https://picsum.photos/315/220?random=8', postViews :1 + 'k' , user: {name : 'Daniel' , type : 'TEAM'}},
        {title: 'Web Design 5',postLikes :175 , cover : 'https://picsum.photos/315/220?random=4', postViews :2 + 'k' , user: {name : 'Nikolay' , type : 'TEAM'}},
        {title: 'Web Design 6',postLikes :106, cover : 'https://picsum.photos/315/220?random=10', postViews :7.8 + 'k' , user: {name : 'Price' , type : 'PRO'}},
        {title: 'Web Design 7',postLikes :50 , cover : 'https://picsum.photos/315/220?random=3' , postViews :1.6 + 'k' , user: {name : 'Soup' , type : 'PRO'}},
        {title: 'Web Design 8',postLikes :14 , cover : 'https://picsum.photos/315/220?random=6' , postViews :1 + 'm' , user: {name : 'Mamad' , type : 'TEAM'}},
        {title: 'Web Design 9',postLikes :82 , cover : 'https://picsum.photos/315/220?random=7', postViews :200, user: {name : 'Amirali' , type : 'TEAM'}},
        {title: 'Web Design 10',postLikes :205 , cover : 'https://picsum.photos/315/220?random=9', postViews :0.9 + 'k' , user: {name : 'Tom' , type : 'PRO'}},
        {title: 'Web Design 11',postLikes :301 , cover : 'https://picsum.photos/315/220?random=11' , postViews :512 , user: {name : 'Dani' , type : 'TEAM'}},
        {title: 'Web Design 12',postLikes :60, cover : 'https://picsum.photos/315/220?random=15', postViews :126 , user: {name : 'Erfun' , type : 'PRO'}},
        {title: 'Web Design 12',postLikes :60, cover : 'https://picsum.photos/315/220?random=12', postViews :126 , user: {name : 'Erfun' , type : 'PRO'}},
        {title: 'Web Design 12',postLikes :60, cover : 'https://picsum.photos/315/220?random=14', postViews :126 , user: {name : 'Erfun' , type : 'PRO'}},
        ],
    }
  },

}
</script>

<style>
ol.cardsBox {
  list-style: none;
  width: 100%;
  border: none;
  padding: 32px 0 4px 0;
  display: flex;
  flex-wrap: wrap;
  grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
}
li.card {
  width: 315px;
  height: 250px;
  margin: 0 38px 36px 0;
}

li.card div.cardPic {
  border: none;
  border-radius: 10px;
  width: 100%;
  height: calc(100% - 30px);
  position: relative;
  z-index: 1;
}

li.card div.cardPic div.hoverTime {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 30%;
  border-radius: 0 0 10px 10px;
  background: rgb(0,0,0);
  background: linear-gradient(0deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0.5301470930168943) 50%, rgba(0,0,0,0) 100%);
  display: flex;
  justify-content: space-between;
  opacity: 0;
  padding-top: 15px;
  transition: opacity 350ms;
}

li.card div.cardPic:hover div.hoverTime {
  opacity: 1;
}

li.card div.cardPic div.hoverTime div.postName {
  color: #fff;
  font-weight: bold;
  font-size: 20px;
  height: 100%;
  padding-left: 20px;
  justify-content: space-evenly;
  line-height: 1.7;
}

li.card div.cardPic div.hoverTime div.postSituation {
  width: 100px;
  padding-right: 20px;
  height: 100%;
  display: flex;
  justify-content: space-between;
}

li.card div.cardPic div.hoverTime div.addToFile ,
li.card div.cardPic div.hoverTime div.likeButton {
  width: 34px;
  height: 34px;
  background-color: #eee;
  border-radius: 5px;
}

li.card div.cardPic div.hoverTime div.addToFile svg ,
li.card div.cardPic div.hoverTime div.likeButton svg {

  fill: #6e6d7a;
  width: 20px;
  margin: 7px;
}



li.card div.user {
  width: 100%;
  height: 24px;
  margin-top: 6px;
  display: flex;
  justify-content: space-between;
}

li.card div.user div.userInfo {
  width: 50%;
  height: 100%;
  border: none;
  display: flex;
}

li.card div.user div.userInfo div.userPic {
  width: 30px;
  padding-left: 7px;
  border-radius: 50%;
}

li.card div.user div.userInfo div.userPic svg path{
  fill: #eeeeee;
}

li.card div.user div.userInfo div.userName {
  color: #000;
  height: 20px;
  font-size: 19px;
  padding: 0 9px;
  line-height: 1.2;
}

li.card div.user div.userInfo div.userType {
  height: 15px;
  padding: 0 5px;
  border-radius: 6px;
  background-color: #9e9ea7;
  color: #fff;
  font-size: 12px;
  font-weight: bold;
  margin: 4px 0;
  transition: background-color 350ms;
}
li.card div.user div.userInfo div.userType:hover {
  background-color: #ea4c89;
}
li.card div.user div.postInfo {
  padding-right: 7px;
  height: 20px;
  border: none;
  display: flex;
  justify-content: space-between;
}

li.card div.user div.postInfo div.like {
  height: 100%;
  cursor: text;
}


li.card div.user div.postInfo div.like svg {
  width: 14px;
  height: 14px;
  fill: #9e9ea7;
  margin: -3px 1px;
  transition: fill 1s;
}

li.card div.user div.postInfo div.like svg:hover {
  cursor: pointer;
  fill: #ea4c89;
}

li.card div.user div.postInfo div.like span {
  color: #3d3d4e;
  font-family: "Adobe Devanagari";
  font-weight: bold;
  margin-left: 2px;
}

li.card div.user div.postInfo div.view {
  height: 100%;
  margin-left: 10px;
  cursor: text;
}


li.card div.user div.postInfo div.view svg {
  width: 14px;
  height: 14px;
  fill: #9e9ea7;
  margin: -3px 1px;
  transition: fill 1s;
  cursor: default;
}

li.card div.user div.postInfo div.view svg:hover {
  fill: #ea4c89;
}

li.card div.user div.postInfo div.view span {
  color: #3d3d4e;
  font-family: "Adobe Devanagari";
  font-weight: bold;
  margin-left: 2px;
}

@media (max-width: 480px) {

}

@media (min-width: 481px) and (max-width: 768px){

}

@media (min-width: 769px) and (max-width: 1024px){

}

@media (min-width: 1025px) and (max-width: 1535px){
  li.card {
    margin: 0 38px 36px 0;
  }
  li.card:nth-child(4n)
  {
    margin-right: 38px;
  }
}

@media (min-width: 1536px){
  li.card {
    margin: 0 38px 36px 0;
  }
  li.card:nth-child(4n)
  {
    margin-right: 0;
  }
}











</style>