## The  gallery on flexbox
### Additionally:
- Adaptive
- Modal window
- Slide
- Settings


### Basic Markup:
```
<html>
    <body ng-controller="deployImage as depImg">
    	<div class="wrapper" id="wrapper" >
          <section >
            <div class="container-gallery container-flex"><!-- flexbox -->
              <div class="item theme-class-default"  ng-repeat = "item in imgItem">
                <div class="img-wrap">
                  <img ng-src="{{item.itemImgSrc}}" ng-click="showPhoto($index);" draggable="false">  
                </div>
                <h6>
                  <a href="">{{item.itemHeadline}}</a>
                </h6>
                <p>{{item.itemDescription}}</p>
                <div class="advance-rule">
                  <a href="{{item.urlReadMore}}" class="a-btn">{{item.readMoreHeadline}}</a>
                </div>
              </div>          
            </div><!--End container-flex-->
          </section>
      </div><!-- end wrapper -->
      <!--hidden elements-->  
      <div class="modal hidden theme-class-default">
        <div class="modal-button">
          <a class="close-button">X</a>
          <a class="navi prev-button hidden" ng-click="showPrev();"></a>
          <a class="navi next-button hidden" ng-click="showNext();"></a>
        </div>
        <div class="modal-content" ng-repeat = "item in imgItem">
          <img  draggable="false"  ng-show="isActive($index)" ng-src="{{item.itemImgSrc}}">
        </div>
      </div>
</html>
```
