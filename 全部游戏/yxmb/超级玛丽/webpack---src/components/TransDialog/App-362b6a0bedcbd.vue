@import '@/scss/variables.scss';

















































































































































































































































































$dialog-z-index: 999999999999999;
button:focus {
  outline: 0;
}

.TransIcon {
  position: fixed !important;
  transition: all 0.2s linear;
  animation: fadeIn 0.2s linear;
  // width: 24px;
  // height: 24px;
  z-index: $dialog-z-index;
  filter: unset;
  width: 32px;
  height: 32px;
  border-radius: 11px;
  border: 1px solid #F1F1F1;
  overflow: hidden;
  img {
    width: 32px;
    height: 32px;
    object-fit: cover;
    pointer-events: none;
  }
}

.TransIcon:hover {
  cursor: pointer;
}

.TransDialog {
  position: fixed !important;
  // transition: all 0.2s linear;
  animation: fadeIn 0.2s linear;
  // width: 392px;
  // height: 448px;
  background: #ffffff;
  border-radius: 16px;
  border: 1px solid #f1f1f1;
  // overflow: auto;
  box-shadow: 0px 8px 40px 0px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  z-index: $dialog-z-index;
  .dragBlock {
    position: absolute;
    top:0;
    left: 0;
    right: 0;
    // height: 60px;

    &:hover {
      cursor: move;
    }

    .top-drap-block, .left-drap-block {
      position: absolute;
      left: 0;
    }
    // defalult
    .top-drap-block {
      right: 0;
      height: 15px;
    }
    .left-drap-block {
      height: 55px;
      right: 120px;
    }

    // preview
    &.preview {
      .left-drap-block {
        width: 20px;
        height: 79px;
        right: 160px;
      }
    }

    // dialog with scale
    &.scale {
      .left-drap-block {
        right: 53px;
        left: 177px;
        height: 40px;
      }
    }
  }
}

.MOJiWebExtensionpanelObject {
  height: 100%;
  width: calc(100% + 5px);
  border: none;
  overflow: hidden;
  // background: #ffffff;
  z-index: $dialog-z-index;
  // 不显示火狐iframe的滚动条
  // &.firefox-object {
  //   width: calc(100% + 15px);
  // }
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
