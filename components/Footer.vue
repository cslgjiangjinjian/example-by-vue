<style type="text/css">
	.footer{width: 100%;background-color: #fff;color: #666;position: fixed;bottom:0;left: 0;z-index: 10;}
		.footer>a{width: 50%;line-height: 1.3rem;padding:0.85rem 0;font-size: .8rem;}
		/*.footer>a:hover{color:#E9665F;}*/
		.footer>a.sxwd{background-size: 1.2rem 1.2rem;background-repeat: no-repeat;background-position: 1.5rem center;}
		.footer>a.sxwdimg{background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAYAAACpSkzOAAAABGdBTUEAALGPC/xhBQAAA4tJREFUSA2tll1Ik2EUx333BdsCRejDMkMskCLIgiDIIsMoJKWoLozyQnDzg8KICCkcSlBSKIabSl0E3fVheVFeeNNFUFBGmBVoVIRagTYst9J99DvTd5vbO1PXA2fnec75n/N/nvM+H1NSltCqq6vX+Xy+l8FgcFhRlAHkgU6ne+R0On8lSqckcsTaKyoqUkm2FrtRr9ePT09Pf6LvR/SINDeEl0wm03XanxlT5DchEbNV7HZ7AboM+B4kczbMYzQaNwoRiXvol09NTR2jfxbsGvRbdHFnZ+eHCE1KiiaRzWbbAdgJcIuACR5G9WPLl2E0UUdHxwHB1NbWmj0ez3m6F5AfYIsgey4+aboZFfmlRPWAnmLZhLiQbSTLnE04FkHO7TU3N3vB1FPeQ3gsyENyZamoOUSsRBI7kFfMOo8ZVSF9Kngh2uVydVOBE2BXoO8w6VDVwkSQnMZoB9BrMBh2t7W1DSwksRamvb39HiSt5NteWVlZKpgQEUvcTP8qzsG0tLTD821TrcRaNovF0oDdHQgEHOIPEUHQCLuB+p5samr6KY5kG99snBw3kfXs3jwdq8mFpASyHur7LFmC6Hg5xDIm/0FZRTHLk7GwL6qRoICJfk8URF71MOcYGBSymoDZbO5NFBBrhyBAjLrVwxsqFsc4iIyBtxroZNH51tLS4tYAxpkgULjnrDh2xjk1DByP92I2ELcK/VEDo2liUmYc7zSdMUZyyzcJlU9W5JGlxWA0hwT24Fiu6Yw3FpI3XFYDgxEwufG4eAtXjC3eGm8hp8IFIMdkSPUKo9wAFnbPVtWYrK6pqdlADqnSGzWXjnJ0ywAtl+F/aX6//6gkUs9RqM8jJnV3s9wqVpUqxmSaw+EwcWTKmfgER+a+mksn9xrGyxjSkQbVsVQ9Ojp6jths5Jo8HWqe0K7gAmyFbBDjKe6l46pzsZoNsJfKXCRuiCf9SnR8+IWVOw+H3HXyaMk7dCMa+K8+8fvA3EXk7OQT3x8dEyYSIzPaxYy66Kazwtt8vzpK+yU6ILbPE54+OTlZh/0MMkFMCZfzk1jcHCJxMrMclMxM/i/8hrALkb9TfVw9I1arNej1elfiy2NS+9Gl6GVgXkNyhImFzw6+cIsjEg87R8dHLSOB1Ds7jNbufIakMSMj4xZxPm1Ign9B0WBWKAe5CMkh4WrIUcpXxoOs4DFP/gvGckvP2/4Cq4JhWMerz5EAAAAASUVORK5CYII=');}
		.footer>a.sxwdimgafter{
			border-bottom: .15rem solid #E9665F;color:#E9665F;padding-bottom:0.7rem;
			background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAYAAACpSkzOAAAABGdBTUEAALGPC/xhBQAABAVJREFUSA2tVl2IW1UQnjk3SU1SrN3dm/hTK0tbKIrgKgiCP1ipKMUtFvWhRTc2crNWUVZEpCgNLYKKstKliRvZZgO++bPah7oPffFBsKCVolVhK1rEarK/rbrbZnPv+J2bZvfm5y67rech55yZb+bLmTMz5zJdxph+LnlTuVL5loT+IKZTzMZnpK46Gstk/vFzx36KRvmUZa0hZd9YIQoGDZoqz1d+g7EtRIbGMvGMML8RC60e4IGBi432vkQiwpO9iS2YeoTkfjhcVzXm2VDQuNklYh7loEpS2XlCWF4WoRuI+UeSUHc8l/vFS9aSaDK1+y5bnAwIbtNgZoSI+HuQ36N3XqLY4PDDGiN9feHS7MyrTPIa7KYNUds6cvnjWqeHqk6Lv+NWYp8t9leQ3AJlVpG6IzZYWHfJ4eQisn7F/f1z8cH8PlbqUWgiNsnnCPf6GqqOqJhKZB2SNP71d0Yw2GXmCnvMXP5EDbyc2cwePoILexIni83zxY/0FWi7BaJSKvEiifRCdowCkfvaD31wajmOW2Hi7xc+QYQPIivvnHg2sVNjXKIpK3ErovwOM4+pa4wdS6VpK8etZKsixn43Ex1Ka71LNM90ABkTMBQ9Zb59+O9WhiuVrekfmhLiIWTrxlJvsktNWInNCNl2nGa0PTv89UodLoXHHz+q9SyVRwK2km5y3O3QUkatdLjoLUUrUWql0zLbEbeYcaoNAZBsxWmcYFiO+Rk0yh1xHGTWpVSXhYRqxGEPDuCEowHk3nqErrj2vcJMC2CziNEDKhQ1iO9uVjZLOnLDP2tpAP/sWkTx12aIj0QojGL8yUdbJ9aRgsANXwAkszhRtA7ht2Eahcr0U3vliNRWZPJCWAOI4lmk4WYvyG8dHyyk/HReue4GaAAoEzldkyswowNIZNx6+vaa8ErnieetTfCBKPEPNV8Kb8gRvRF2dDP8X4bY5ce1I6XErSN3TUZ41G0Vwnvcx+0KqSSdDolDSTwt5zvCbZ/W3Cm3rzG9iTO1VWh+f01xufP4n2degW0nruRd/XTU/LhZYUbWHkQqjgk5L4z39uyqKVc6T6R6HhBxXgfJ6Y7Q1W957V0izayEuhHCc+JwHonxjBe0nHXR2v2gIzwCH3Mozh2N3w0gXxylVPJeEXtEhxGF/CHa+d72TP73RUTz6lxfsu3Cv85eJuclZNl5Nni7mc1/2YisI9LKomVtYCp/XP1e4AtovSPVzyk+YVaMsxSNyszcdNwm1YUn/yE42InCXI3QnyTDeCyWGVqoHS9ZE5FWInMULrVHxxvbTq9B85rPMMsB87rOAqfTlWZ9VdKSyAuuFrJs060er//1aFe4BvoLlzuGMH3Rfij/DU6ju/SS4z8eT3qWgUOaUQAAAABJRU5ErkJggg==');}
		.footer>a.ysfx{background-size: 1.2rem 1.2rem;background-repeat: no-repeat;background-position: 1.5rem center;}
		.footer>a.ysfximg{background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABsAAAAaCAYAAABGiCfwAAAABGdBTUEAALGPC/xhBQAABAhJREFUSA2dll9I5FUUx+f3G8eRCsN6cgSphE2LhYVxUBd8UKl9KFMShHrqIfyzLtHuVr5s4KuhuCCOfyhYIp8i0B6KctNgn0znIaJCC1q0NOhBDDfUSWc/38vvDr/57fxc1wOXc88533POPfd37r0/J/IQGhgYOHd0dNR5fHz8EtBqx3EScsnlcluwDdd1F6LR6NzExMS69CeRE2bs7+9PkuAjgraGYfx6FrFI4g8mJyczfr1//kCyoaGhku3t7ZskuQyQGM4OfB55PhaL/eJVJEOCil9Efg17B7wCnkOfrqysfJc4/yMXUEEyqqkgwBcgWhj7OI4RZHhmZma3wCsg9PT0PAl2EOxVTGWMJba2iyq10Dzlk6mira2tb7G04PgXvHN6eno1jzzFpLe3tx7YHEmr4EuJROJlf4UlNoa2jrlJRLKGqakpJcxTX1/fqwS5zkih/BeMFvIhC/rRgrQ4cA3Iy+BavJhXrN1UpmZg+1ZQHhCkOVgR2zSC7bp18vEs+H7wn/h0EVVIsjvo4mxnyjaNK5C6DoafMxZMxEovYTOJsGcY7yC/B9+ExwiaJvgLzPOkGIqFwvFiG5tLVc/j0IpxBz6c9/Am6Mw2YP+ura2tgUDjNMxoaWlpEsg2o5TxFqOAFMuL2aqzKqOLssNDzYd0nT66yp7o7u4+8rCR8fHxf9B95skXrN5yL9a8ZF0K4q53M+hGMAYp/YT+e+T18vLy23695thyni4btElmMV+K2xzqxmopdGDFg8QK3wjqJNM0tbC3NSfnN+JBojl+JpHUJodLdv9dF8QXlWmIaxjU+k/hvwb/uBiQRej+NLeNuOlGTU5LSkSQUfCPM35ltFP9f8X8aSJzjsGbq0sNUpC9mJPVsXUx5jckU9Es3zFFd/5m7UF+eHj4jKe7K67KNjTJZrMFZ0W6IPFdn2VxFdLD3x8ZGbkXxPhluvA5T74rzqvgLmjCSu0RkFiUSGC+NthNKvq7KMinBN8lkRz6vhE1iG35Dt3eUoZROp3+HVsj3+Iifrbti8L1gmB4naGzeYsRcbm31nBc1PbAB6U8iWiGZQ70nydhZGML34SVEfNre6mbbtQLi4F8uau6RAUOI6r/FMxP8MfCMNKTpM3j5mBrbpLpVsaYRtbDN8flWyVjCJ1HXxOPx9X6J5G52ijAtL2AJpkmesphSxirGMthFfIgNmGv1t0ovzAC84Ns8FcsJv9SS3HW3wIbzM/ZZv2J/YFOb16NvlvUD1hdXd1vb2+f3dvbexp9E6MZYG99fX1tMpl0Ghsbj1Op1MHKysqh36/YPJPJ7OJTh00vQhz5q4LK/E56vfXwsQ2tfv0Z51n86kKT2aDe49rhPRPmJ5UFPGHtj8A/vw/wCNbohpxSLgAAAABJRU5ErkJggg==');}
		.footer>a.ysfximgafter{
			border-bottom: .15rem solid #E9665F;color:#E9665F;padding-bottom:0.7rem;
			background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABsAAAAaCAYAAABGiCfwAAAABGdBTUEAALGPC/xhBQAABFdJREFUSA2dVl1sVEUUPmdud7cFRcHeNZZkA5LgX0xMoEFNfFCiPqCWSELUF7ZEd7tijIg/L5r0VVOCSW3LrlBao/HBmFBfjH9g4hMCD8aoAU1oVIqw9TdYpdt7j9+Z3ene7t5t0Uluzsz5+2bOnDnnMi0xyrueWB8Gs1sppHuZKENMXdZEaEqIfiBDHxsvedgfeuP0Eq5g2mKUCzs2hCG/SiL3tFBZyGY+Yoy84I+Mn1woqK+awKS/v618bvI1gDyJnTMz/QYyYYQmJJH4RiQxpebMlS4OgltCCR8ikh4RWglnAsGwf92aZ7i/f64OU50tAPu9UFg5G8y8B5C74e4fZtnXJqlXVpVKfzQaRte/5nJXzfGlF0V4N/Da4fRo0lu27eqREWy0PubB7ImmznykQDjNWSZvq18cPVFXXXpWzu/cKBQcxilXK6Dftfa+6AnnwS7ks6+LyC4FMtyxqXP//rNR9+W+3gcg34OvG0Z/IlwnhMzL1xZHv4zqTff1rQ7l72MWkHkoXRx7ysktmCaDBHQcAb9k2NzVeKLzud4BonCPM3KUiSvEUkgXxw86nlI9Ie7ycyZJsUfdLmmMCjXrqskg+5qA+nrvd0A49UlkzNMweg70RyFJ4ATDv+R7b1Y/bqgPvW/1aTO6JjDlws4bNL016zQZnIGjLGE1DMyf+pu3bEJYBv3S+N6OJG9AWM5BLxmSZJ2+o+pLfapvfavKN6EEPVUFnojPOt6oco/NEG/fHlR1ia4cPFTG6d7SdUh0m+M7WvXFE1auRQHDaGWwE7wjpU1D6DOc4LSsoE+aZYxIIVZElSYZGLj/9y2/htEGxYxa6IONM0iXxh6N40/nsjcGJI9bmciHcTrieV9TGOhmMio3mNla5ypDnFEjr5zPPgsgvEFZhVCe8il1oFFH1/M+axg2G+MUW/EUKBTZC/ly7Phb0Ae5VJqJ008kZ9osX9iWLoNqNl/r4gyiPMnlEkj3lyyP+W1/hd+N7PwuqhOdV2ZpTW09qRT1FW0CgyuVBW9FeY1jOiFrteAq30jyeR4Y+KtRJ7pGobhe18CYVGq0H+kkZKo9AV3FD5EQWY6N4UF3Fos/x2tFuELbrL7R+wWYYa+W8tKj1Tui2jRNDx/83iNzu5dsuxOANu2blGoM7SCYPox7DQx1jCnb+COjp7DVIxoebRPKXGx0lg4du2bwwE+L6agMreoxBLAd2f6BK+o2G7XDYgco6Lxbi+hijsq57Jvn8zu+QrIsW0xPmDarHBGoPmzMLZityuiwuhPtR9omWjlC7G6FbN3FVGV5Kx3la/iU4gA27XVuwXRiWzkanvYh7UetTuh30R0dkspobVS7VgMgX1iZyBangw3Ux//9Lah7qM+QbJk5nj2DSFQ8bl+n97YATFUv54cnPTx8se629exCLvsOisAjuDfbsZvAnOl//pVzhjFUO7pQ8qaWYM5Gm6vteZGfVNzrFU5+uRSA7/4LUkzVoWyPzAkAAAAASUVORK5CYII=');}

	/*.footer>a:focus{border-bottom: .15rem solid #E9665F;color:#E9665F;padding-bottom:0.7rem;}*/
	/*border为1像素真是麻烦啊~*/
	.b_r_1{position: relative;}
	.b_r_1:after{
		content:'';
		position: absolute;
		width: 200%;
		height: 200%;
		border-right:1px solid #ddd;
		top: 0;
		left: 0;
		-webkit-transform:scaleX(.5);
        -ms-transform:scaleX(.5);
        -o-transform:scaleX(.5);
        transform:scaleX(.5);
		transform-origin:0 0;
	}
	@media (min--moz-device-pixel-ratio: 1.5), (-webkit-min-device-pixel-ratio: 1.5), (min-device-pixel-ratio: 1.5), (min-resolution: 144dpi), (min-resolution: 1.5dppx), (-ms-high-contrast:active), (-ms-high-contrast:none) {
		.b_r_1:after{
			-webkit-transform:scaleX(.5);
	        -ms-transform:scaleX(.5);
	        -o-transform:scaleX(.5);
	        transform:scaleX(.5);
		}
	}
	 /*@media (-webkit-device-pixel-ratio: 1.5){
		 .b_r_1:after{
			-webkit-transform:scaleX(.6666);
            -ms-transform:scaleX(.6666);
            -o-transform:scaleX(.6666);
            transform:scaleX(.6666);
 		}
	 }
	 @media (-webkit-device-pixel-ratio: 3){
		 .b_r_1:after{
			-webkit-transform:scaleY(.3333);
            -ms-transform:scaleY(.3333);
            -o-transform:scaleY(.3333);
            transform:scaleY(.3333);
 		}
	 }*/
</style>
<template>
	<footer class="footer clear">
		<a href="javascript:;" class="left b_r_1 text-center sxwd sxwdimg" :class="{'sxwdimgafter':isSelect=='xswd'}" @click="showTab('xswd')">
			销售问答
		</a>
		<a href="javascript:;" class="left text-center ysfx ysfximg" :class="{'ysfximgafter':isSelect=='ysfx'}" @click="showTab('ysfx')">
			友商分析
		</a>
	</footer>
</template>
<script type="text/javascript">
	export default {
		data(){
			return {
				footer:'this is footer',
				isSelect:"sxwd"
			}
		},
		methods:{
			showTab:function(route){
				this.isSelect = route;
				window.location.hash = '#!/'+ route;
			}
		},
		ready(){
			console.log('footer:'+this.$parent.ROUTE);
				this.isSelect = this.$parent.ROUTE;
		},
		watch:{
			"$parent.ROUTE":function(newval){
				console.log('footerwatch:'+this.$parent.ROUTE);
				this.isSelect = this.$parent.ROUTE;
			}
		}
	}
</script>
