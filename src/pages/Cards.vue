<template>
  <f7-page>
    <f7-navbar title="Cards" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>Cards, along with List View, is a one more great way to contain and orginize your information. Cards contains unique related data, for example, a photo, text, and link all about a single subject. Cards are typically an entry point to more complex and detailed information.</f7-block>
    <f7-block-title>SIMPLE CARDS</f7-block-title>
    <f7-card
      content="This is simple card with plain text. But card could contain its own header, footer, list view, image, and any elements inside."
    ></f7-card>
    <f7-card
      title="Card header"
      content="Card with header and footer. Card header is used to display card title and footer for some additional information or for custom actions."
      footer="Card Footer"
    ></f7-card>
    <f7-card
      content="Another card. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse feugiat sem est, non tincidunt ligula volutpat sit amet. Mauris aliquet magna justo."
    ></f7-card>
    <f7-block-title>STYLE CARDS</f7-block-title>
    <f7-card>
      <f7-card-header
        valign="bottom" class="color-white no-border card-img-header1">Journey To Mountains</f7-card-header>
      <f7-card-content>
        <p class="color-gray">Posted on January 21, 2015</p>
        <p>Quisque eget vestibulum nulla. Quisque quis dui quis ex ultricies efficitur vitae non felis. Phasellus quis nibh hendrerit...</p>
      </f7-card-content>
      <f7-card-footer>
        <f7-link href="#">Like</f7-link>
        <f7-link href="#">Read more</f7-link>
      </f7-card-footer>
    </f7-card>
    <f7-card>
      <f7-card-header
        valign="bottom" class="color-white no-border card-img-header2">Journey To Mountains</f7-card-header>
      <f7-card-content>
        <p class="color-gray">Posted on January 21, 2015</p>
        <p>Quisque eget vestibulum nulla. Quisque quis dui quis ex ultricies efficitur vitae non felis. Phasellus quis nibh hendrerit...</p>
      </f7-card-content>
      <f7-card-footer>
        <f7-link href="#">Like</f7-link>
        <f7-link href="#">Read more</f7-link>
      </f7-card-footer>
    </f7-card>
    <f7-block-title>FACEBOOK CARDS</f7-block-title>
    <f7-card class="card-facebook-card">
      <f7-card-header class="no-border">
        <div class="facebook-avatar"><img src="../assets/photo1.jpg" alt="photo" width="34" height="34"></div>
        <div class="facebook-name">John Doe</div>
        <div class="facebook-date">Monday at 3:47 PM</div>
      </f7-card-header>
      <f7-card-content class="card-no-padding">
        <img src="../assets/card3.jpg" width="100%" alt="photo">
      </f7-card-content>
      <f7-card-footer class="no-border">
        <f7-link href="#">Like</f7-link>
        <f7-link href="#">Comment</f7-link>
        <f7-link href="#">Read more</f7-link>
      </f7-card-footer>
    </f7-card>
    <f7-card class="card-facebook-card">
      <f7-card-header class="no-border">
        <div class="facebook-avatar"><img src="../assets/photo1.jpg" alt="photo" width="34" height="34"></div>
        <div class="facebook-name">John Doe</div>
        <div class="facebook-date">Monday at 3:47 PM</div>
      </f7-card-header>
      <f7-card-content>
        <p>What a nice photo i took yesterday!</p>
        <img src="../assets/card3.jpg" width="100%" alt="photo">
        <p class="color-gray">Likes: 112    Comments: 43</p>
      </f7-card-content>
      <f7-card-footer class="no-border">
        <f7-link href="#">Like</f7-link>
        <f7-link href="#">Comment</f7-link>
        <f7-link href="#">Read more</f7-link>
      </f7-card-footer>
    </f7-card>
    <f7-block-title>CARD WITH LIST VIEW</f7-block-title>
    <f7-card>
      <f7-card-content>
        <f7-list>
          <f7-list-item
            media="<i class='icon icon-f7'></i>"
            link="#"
            title="Link 1"
          ></f7-list-item>
          <f7-list-item
            media="<i class='icon icon-f7'></i>"
            link="#"
            title="Link 2"
          ></f7-list-item>
          <f7-list-item
            media="<i class='icon icon-f7'></i>"
            link="#"
            title="Link 3"
          ></f7-list-item>
          <f7-list-item
            media="<i class='icon icon-f7'></i>"
            link="#"
            title="Link 4"
          ></f7-list-item>
          <f7-list-item
            media="<i class='icon icon-f7'></i>"
            link="#"
            title="Link 5"
          ></f7-list-item>
        </f7-list>
      </f7-card-content>
    </f7-card>
    <f7-card>
      <f7-card-header>New Releases:</f7-card-header>
      <f7-card-content>
        <f7-list media-list class="card-media-list">
          <f7-list-item
           media="<img src='./static/image/photo2.jpg' width='44'>"
           title="Yellow Submarine"
           subtitle="Beatles"
          ></f7-list-item>
          <f7-list-item
           media="<img src='./static/image/photo3.jpg' width='44'>"
           title="Don't Stop Me Now"
           subtitle="Queen"
          ></f7-list-item>
          <f7-list-item
           media="<img src='./static/image/photo4.jpg' width='44'>"
           title="Billie Jean"
           subtitle="Michael Jackson"
          ></f7-list-item>
        </f7-list>
      </f7-card-content>
      <f7-card-footer>
        <span>January 20, 2015</span>
        <span>5 comments</span>
      </f7-card-footer>
    </f7-card>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">
.card-img-header1{
  height: 40vw;
  background-image: url('../assets/card1.jpg');
  background-size: cover;
  background-position: center;
}
.card-img-header2{
  height: 40vw;
  background-image: url('../assets/card2.jpg');
  background-size: cover;
  background-position: center;
}
.card-facebook-card{
  .card-header{
    display: block;
    padding: 10px;
  }
  .facebook-avatar{
    float: left;
  }
  .facebook-name{
    margin-left: 44px;
    font-size: 14px;
    font-weight: 500;
  }
  .facebook-date{
    margin-left: 44px;
    font-size: 13px;
    color: #8e8e93;
  }
  .card-footer{
    background: #fafafa;

    a{
      color: #81848b;
      font-weight: 500;
    }
  }
  .card-content{
    img{
      display: block;
    }
  }
}
.card-no-padding{
  .card-content-inner{
    padding: 0;
  }
}
.card-media-list{
  .item-content{
    .item-inner{
      .item-title-row{
        .item-title{
          font-weight: 500;
        }
      }
    }
  }
}
</style>
