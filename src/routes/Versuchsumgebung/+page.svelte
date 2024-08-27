
	<div class="iceberg">
		<span></span>
	</div>

<style>

.iceberg {
  position: relative;
  z-index: 0;
  width: 0;
  height: 0;
  border-left: 185px solid transparent;
  border-right: 185px solid transparent;
  border-bottom: 185px solid #004AAD;
  animation: float 4s ease-in-out infinite;
}
.iceberg::before {
  content: '';
  display: block;
  position: absolute;
  top: 185px;
  left: -185px;
  width: 0;
  height: 0;
  border-left: 95px solid transparent;
  border-right: 95px solid transparent;
  border-top: 95px solid lightblue;
}
.iceberg::after {
  content: '';
  display: block;
  position: absolute;
  top: 185px;
  width: 0;
  height: 0;
  border-left: 95px solid transparent;
  border-right: 95px solid transparent;
  border-top: 95px solid lightblue;
}
.iceberg span {
  position: absolute;
  z-index: 1;
  left: 0;
  top: 0;
  margin-left: -100px;
  display: block;
  width: 0;
  height: 0;
  border-left: 185px solid transparent;
  border-right: 185px solid transparent;
  border-bottom: 185px solid darkblue;
  animation: float2 4s ease-in-out infinite;
}
.iceberg span::before {
  content: '';
  display: block;
  position: absolute;
  top: 185px;
  margin-left: -5px;
  width: 0;
  height: 0;
  border-left: 95px solid transparent;
  border-right: 95px solid transparent;
  border-top: 95px solid #89cff3;
  z-index: -1;
}
.iceberg span::after {
  content: '';
  display: block;
  position: absolute;
  top: 185px;
  margin-left: -185px;
  z-index: -1;
  width: 0;
  height: 0;
  border-left: 95px solid transparent;
  border-right: 95px solid transparent;
  border-top: 95px solid #89cff3;
}
@-moz-keyframes float {
  0% {
    transform: translateY(15px);
  }
  50% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(15px);
  }
}
@-webkit-keyframes float {
  0% {
    transform: translateY(15px);
  }
  50% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(15px);
  }
}
@-o-keyframes float {
  0% {
    transform: translateY(15px);
  }
  50% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(15px);
  }
}
@keyframes float {
  0% {
    transform: translateY(15px);
  }
  50% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(15px);
  }
}
@-moz-keyframes float2 {
  0% {
    transform: translateY(5px);
  }
  50% {
    transform: translateY(-5px);
  }
  100% {
    transform: translateY(5px);
  }
}
@-webkit-keyframes float2 {
  0% {
    transform: translateY(5px);
  }
  50% {
    transform: translateY(-5px);
  }
  100% {
    transform: translateY(5px);
  }
}
@-o-keyframes float2 {
  0% {
    transform: translateY(5px);
  }
  50% {
    transform: translateY(-5px);
  }
  100% {
    transform: translateY(5px);
  }
}
@keyframes float2 {
  0% {
    transform: translateY(5px);
  }
  50% {
    transform: translateY(-5px);
  }
  100% {
    transform: translateY(5px);
  }
}
</style>