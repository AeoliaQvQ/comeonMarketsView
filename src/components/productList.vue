<template>
  <div class="hello">

  		<div class="container productList">
    		<leftCategory></leftCategory>
  			<div class="span18 last">
  				<div id="result" class="result table clearfix">
  					<ul>
            <li>
              <router-link to="/shopdetail"> <img  src="./../assets/shop.jpg"
            									style="width: px;height:170px; display: inline-block;"/>
                              <span style='color:green'>超级大内内</span> <span class="price"> 商城价：
  											￥1234元
  									</span>
               </router-link>

           </li>
           <li>
             <router-link to="/shopdetail"> <img  src="./../assets/shop.jpg"
                            style="width: px;height:170px; display: inline-block;"/>
                             <span style='color:green'>超级大内内</span> <span class="price"> 商城价：
                      ￥1234元
                  </span>
              </router-link>

          </li>
          <li>
            <router-link to="/shopdetail"> <img  src="./../assets/shop.jpg"
                            style="width: px;height:170px; display: inline-block;"/>
                            <span style='color:green'>超级大内内</span> <span class="price"> 商城价：
                      ￥1234元
                  </span>
             </router-link>

         </li>
         <li>
           <router-link to="/shopdetail"> <img  src="./../assets/shop.jpg"
                           style="width: px;height:170px; display: inline-block;"/>
                           <span style='color:green'>超级大内内</span> <span class="price"> 商城价：
                     ￥1234元
                 </span>
            </router-link>

        </li>
        <li>
          <router-link to="/shopdetail"> <img  src="./../assets/shop.jpg"
                          style="width: px;height:170px; display: inline-block;"/>
                          <span style='color:green'>超级大内内</span> <span class="price"> 商城价：
                    ￥1234元
                </span>
           </router-link>

       </li>
          	</ul>
  				</div>
  				<div class="pagination">
          <span>第1页
          					</span>
                      <span>{{msg}}   </span>
  				</div>

  			</div>
  		</div>
    </div>

      </div>
</template>

<script>
import leftCategory from './leftCategory'
import Vue from 'vue'
import VueRouter from 'vue-router'
import VueSource from 'vue-resource'

Vue.use(VueRouter)
Vue.use(VueSource)
export default {
  name: 'hello',
  data () {
           return{
            msg: "this.message"
  }
  }, created (){
      this.$emit('viewIn',"购彩资讯");
      this.$http.get('http://localhost:9090/user/message') .then(
        function(response){
        this.msg = response.bodyText;
        },
        function(response){
          console.log("error")
        }
      )
    } ,
    components: {
     leftCategory
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* ---------- ProductList ---------- */

div.productList .filter {
	margin-bottom: 4px;
}

div.productList .filter .title {
	height: 30px;
	line-height: 30px;
	padding-left: 10px;
	color: #6d6d6d;
	font-size: 14px;
	font-weight: bold;
	font-family: "Microsoft YaHei";
	border: solid 1px #e4e4e4;
}

div.productList .filter .content {
	padding: 0px 10px;
	border-left: solid 1px #e4e4e4;
	border-right: solid 1px #e4e4e4;
}

div.productList .filter dl {
	width: 678px;
	line-height: 30px;
	position: relative;
	overflow: hidden;
	*zoom: 1;
	border-bottom: dotted 1px #e8e8e8;
}

div.productList .filter dl.last {
	border-bottom: none;
}

div.productList .filter dt {
	width: 80px;
	float: left;
	margin-right: 8px;
	text-align: right;
	white-space: nowrap;
	overflow: hidden;
	cursor: default;
}

div.productList .filter dd {
	float: left;
	margin-right: 12px;
	color: #1859a5;
	white-space: nowrap;
}

div.productList .filter dd a {
	line-height: 30px;
	padding: 2px 4px;
	color: #2953a5;
}

div.productList .filter dd a.current {
	color: #ffffff;
	background-color: #ff6600;
}

div.productList .filter .moreOption {
	width: 12px;
	height: 30px;
	line-height: 30px;
	display: none;
	margin-right: 0px;
	position: absolute;
	top: 0px;
	right: 0px;
	color: #7d7d7d;
	cursor: pointer;
	overflow: hidden;
	background: url(../assets/product.gif) -210px -270px no-repeat;
}

div.productList .filter dd.close {
	background: url(../assets/product.gif) -210px -300px no-repeat;
}

div.productList .filter .moreFilter {
	line-height: 6px;
	background: url(../assets/product.gif) 0px 0px repeat-x;
}

div.productList .filter .moreFilter a {
	width: 108px;
	height: 27px;
	line-height: 22px;
	display: block;
	margin: 0px auto;
	text-align: center;
	outline: none;
	blr: expression(this.hideFocus = true);
	background: url(../assets/product.gif) 0px -480px no-repeat;
}

div.productList .filter .moreFilter .close {
	background: url(../assets/product.gif) -120px -480px no-repeat;
}

div.productList .bar {
	margin-bottom: 10px;
	color: #434343;
	-webkit-border-radius: 3px;
	-moz-border-radius: 3px;
	border-radius: 3px;
	border: solid 1px #dddddd;
}

div.productList .bar .layout {
	height: 26px;
	line-height: 26px;
	padding: 8px 0px 8px 8px;
	border-bottom: dotted 1px #dddddd;
	background: url(../assets/product.gif) 0px -30px repeat-x;
}

div.productList .bar .layout label {
	float: left;
	margin-right: 8px;
}

div.productList .bar .layout a {
	float: left;
	padding: 1px;
	margin-right: 10px;
	outline: none;
	blr: expression(this.hideFocus = true);
	cursor: pointer;
	border: solid 1px #cccccc;
	background-color: #ffffff;
}

div.productList .bar .layout a:hover {
	border: solid 1px #f9ad75;
}

div.productList .bar .layout a.current {
	border: solid 1px #f9ad75;
}

div.productList .bar .layout a span {
	min-width: 22px;
	_width: 22px;
	_white-space: nowrap;
	height: 22px;
	line-height: 22px;
	display: block;
	margin-right: 0px;
	text-align: center;
	background: url(../assets/product.gif) 0px -90px repeat-x;
}

div.productList .bar .layout a.current span {
	background: url(../assets/product.gif) 0px -120px repeat-x;
}

div.productList .bar .layout .tableType span {
	background: url(../assets/product.gif) 0px -510px no-repeat;
}

div.productList .bar .layout .listType span {
	background: url(../assets/product.gif) -60px -510px no-repeat;
}

div.productList .bar .layout .currentTable {
	border: solid 1px #f9ad75;
}

div.productList .bar .layout .currentTable span {
	background: url(../assets/product.gif) -30px -510px no-repeat;
}

div.productList .bar .layout .currentList {
	border: solid 1px #f9ad75;
}

div.productList .bar .layout .currentList span {
	background: url(../assets/product.gif) -90px -510px no-repeat;
}

div.productList .bar .layout .page {
	float: right;
	margin-right: 0px;
}

div.productList .bar .layout .page span {
	padding: 0px 6px;
}

div.productList .bar .sort {
	height: 26px;
	padding: 8px 0px 8px 8px;
	border-bottom: dotted 1px #dddddd;
}

div.productList .bar .sort a:hover {
	color: #ff6600;
	background-color: #eeeeee;
}

div.productList .bar .sort a.current {
	color: #000000;
	background-color: #eeeeee;
}

div.productList .bar .sort .orderSelect {
	float: left;
	cursor: default;
}

div.productList .bar .sort .orderSelect span {
	width: 100px;
	height: 22px;
	line-height: 22px;
	display: block;
	padding: 0px 6px;
	border: solid 1px #cccccc;
	background: url(../assets/product.gif) right -330px no-repeat;
}

div.productList .bar .sort .popupMenu {
	width: 112px;
	display: none;
	position: absolute;
	-webkit-box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.1);
	-moz-box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.1);
	box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.1);
	border: 1px solid #cccccc;
	background-color: #ffffff;
}

div.productList .bar .sort .popupMenu ul {
	z-index: 100;
	padding: 1px;
}

div.productList .bar .sort .popupMenu li {
	height: 24px;
	vertical-align: middle;
}

div.productList .bar .sort .popupMenu a {
	height: 24px;
	line-height: 24px;
	*line-height: 25px;
	padding: 0px 5px;
	display: block;
	float: none;
	overflow: hidden;
	outline: none;
	blr: expression(this.hideFocus = true);
	-webkit-border-radius: 1px;
	-moz-border-radius: 1px;
	border-radius: 1px;
}

div.productList .bar .sort .asc, div.productList .bar .sort .currentAsc, div.productList .bar .sort .desc, div.productList .bar .sort .currentDesc  {
	height: 22px;
	line-height: 22px;
	display: block;
	float: left;
	padding: 0px 15px 0px 6px;
	outline: none;
	blr: expression(this.hideFocus = true);
	border-top: solid 1px #cccccc;
	border-right: solid 1px #cccccc;
	border-bottom: solid 1px #cccccc;
}

div.productList .bar .sort .asc {
	background: url(../assets/product.gif) right -360px no-repeat;
}

div.productList .bar .sort .currentAsc {
	background: url(../assets/product.gif) right -390px no-repeat;
}

div.productList .bar .sort .desc {
	background: url(../assets/product.gif) right -420px no-repeat;
}

div.productList .bar .sort .currentDesc {
	background: url(../assets/product.gif) right -450px no-repeat;
}

div.productList .bar .sort input {
	width: 38px;
	height: 22px;
	line-height: 22px;
	padding: 0px;
	margin: 0px 4px;
	#margin: -1px 4px;
	_margin: -1px 4px;
	text-align: center;
	vertical-align: middle;
	ime-mode: disabled;
	border: 1px solid #cccccc;
}

div.productList .bar .sort input:disabled {
	background-color: #ffffff;
}

div.productList .bar .sort button {
	height: 24px;
	line-height: 24px;
	display: none;
	padding: 0px 4px;
	color: #666666;
	font-size: 12px;
	vertical-align: middle;
	cursor: pointer;
	_overflow-x: visible;
	border: 1px solid #cccccc;
	background-color: #f6f6f6;
}

div.productList .bar .tag {
	height: 30px;
	line-height: 30px;
	padding: 0px 8px;
}

div.productList .result dl {
	line-height: 30px;
	padding: 10px;
}

div.productList .result dt {
	color: #843d11;
	font-size: 14px;
	font-weight: bold;
	font-family: "Microsoft YaHei";
}

div.productList .table {
	padding: 0px 2px;
	margin-bottom: 10px;
	-webkit-border-radius: 3px;
	-moz-border-radius: 3px;
	border-radius: 3px;
	border: solid 1px #dddddd;
}

div.productList .table li {
	width: 176px;
	height: 246px;
	line-height: 20px;
	float: left;
	overflow: hidden;
	border-bottom: solid 1px #e4e4e4;
}

div.productList .table li.last {
	border-bottom: none;
}

div.productList .table li a {
	height: 240px;
	display: block;
	padding: 3px;
}

div.productList .table li a:hover {
	background-color: #f6f6f6;
}

div.productList .table span {
	display: block;
}

div.productList .table .price {
	line-height: 30px;
	color: #c4161c;
	font-size: 14px;
	font-weight: bold;
}

div.productList .table .price del {
	margin-left: 6px;
	color: #a5a5a5;
	font-size: 11px;
	font-weight: normal;
	text-decoration: line-through;
}

div.productList .list {
	margin-bottom: 10px;
}

div.productList .list li {
	height: 170px;
	line-height: 22px;
	padding: 5px 0px;
	overflow: hidden;
	border-bottom: solid 1px #e4e4e4;
}

div.productList .list img {
	float: left;
}

div.productList .list span {
	display: block;
	float: left;
	padding-left: 20px;
}

div.productList .list .price {
	line-height: 30px;
	float: right;
	color: #c4161c;
	font-size: 14px;
	font-weight: bold;
}

div.productList .list .price del {
	margin-left: 10px;
	color: #a5a5a5;
	font-size: 11px;
	font-weight: normal;
	text-decoration: line-through;
}
</style>
