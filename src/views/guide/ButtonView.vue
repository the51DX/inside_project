<template>
  <div class="button">
    <title-input title="Button" />
    <div class="guide-txt__wrap">
      <h4>버튼 컴포넌트 : ButtonCmp</h4>
      <div class="guide-txt-box">
        <h5>1. btnType</h5>
        <ol>
          <li>btnType : true (button 태그 사용)</li>
          <li>btnType : false (a 태그 사용)</li>
        </ol>
      </div>
      <div class="guide-txt-box">
        <h5>2. ButtonCmp : typeClass</h5>
        <p>
          typeClass(button태그) & colorClass(a태그)를 선택 후 색상 작성
          ex.bgBtn="base" 하면 이중클래스(bg-base) 완성
        </p>
        <ol>
          <li>bgBtn : 배경색만 있는 버튼</li>
          <li>bdBtn : 테투리(선)만 있는 버튼</li>
          <li>hvBtn : hover 시 배경색 생기는 버튼</li>
        </ol>
      </div>
      <div class="guide-txt-box">
        <h5>3. ButtonCmp : sizeClass</h5>
        <p>
          sizeClass & fontSizeClass 를 선택 후 사이즈 작성 ex.btnSize="large"
          하면 이중클래스(btn-large) 완성
        </p>
        <ol>
          <li>large</li>
          <li>medium</li>
          <li>small</li>
        </ol>
      </div>
      <div class="guide-txt-box">
        <h5>4. ButtonCmp : btnTxt</h5>
        <p>
          btnTxt 사용 시 btn-txt 클래스 적용 , <br />
          btnTxt 미 사용 시 hidden 클래스 적용
        </p>
      </div>
      <div class="guide-txt-box">
        <h5>5. ButtonCmp : icon</h5>
        <ol>
          <li>
            positionClass 를 선택
            <ol>
              <li>iconPositionRight : icon-right</li>
              <li>iconPositionCenter : icon-center</li>
              <li>iconPositionLeft : icon-left</li>
            </ol>
          </li>
        </ol>
      </div>
      <div class="guide-txt-box">
        <h5>6. ButtonCmp : useUrl</h5>
        <p>useUrl : 새 페이지 이동 x (기존 페이지에서 이동)</p>
      </div>
      <div class="guide-txt-box">
        <h5>6. ButtonCmp : Icon Button</h5>
        <p>첫번째 버튼 : @click="addNoteMove()"</p>
        <p>두번째 버튼 : @click="$router.push('/home')"</p>
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp bgBtn="base" btnSize="large" btnTxt="default" />
        <ButtonCmp bgBtn="dark" btnSize="large" btnTxt="default" />
        <ButtonCmp bgBtn="disabled" disabled btnSize="large" btnTxt="default" />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="default-icon-right"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="default-icon-right"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="large"
          iconPositionRight="right"
          btnTxt="default-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="default-icon-center"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="default-icon-center"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="default-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="default-icon-left"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="default-icon-left"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="default-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp bdBtn="base" btnSize="large" btnTxt="border" />
        <ButtonCmp bdBtn="dark" btnSize="large" btnTxt="border" />
        <ButtonCmp bdBtn="disabled" disabled btnSize="large" btnTxt="border" />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="border-icon-right"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="border-icon-right"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="large"
          iconPositionRight="right"
          btnTxt="defauborderlt-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="border-icon-center"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="border-icon-center"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="border-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="border-icon-left"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="border-icon-left"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="border-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp hvBtn="base" btnSize="large" btnTxt="default" />
        <ButtonCmp hvBtn="disabled" disabled btnSize="large" btnTxt="default" />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="hover-icon-right"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="large"
          iconPositionRight="right"
          btnTxt="hover-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="hover-icon-center"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="hover-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="hover-icon-left"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="hover-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp bgBtn="base" btnSize="medium" btnTxt="default-medium" />
        <ButtonCmp bgBtn="dark" btnSize="medium" btnTxt="default-medium" />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="medium"
          btnTxt="default-medium"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="medium"
          iconPositionRight="right"
          btnTxt="default-medium-icon-right"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="medium"
          iconPositionRight="right"
          btnTxt="default-medium-icon-right"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionRight="right"
          btnTxt="default-medium-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="medium"
          iconPositionCenter="center"
          btnTxt="default-medium-icon-center"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="medium"
          iconPositionCenter="center"
          btnTxt="default-medium-icon-center"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionCenter="center"
          btnTxt="default-medium-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="medium"
          iconPositionLeft="left"
          btnTxt="default-medium-icon-center"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="medium"
          iconPositionLeft="left"
          btnTxt="default-medium-icon-center"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionLeft="left"
          btnTxt="default-medium-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp bdBtn="base" btnSize="medium" btnTxt="border-medium" />
        <ButtonCmp bdBtn="dark" btnSize="medium" btnTxt="border-medium" />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="medium"
          btnTxt="border-medium"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="medium"
          iconPositionRight="right"
          btnTxt="border-medium-icon-right"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="medium"
          iconPositionRight="right"
          btnTxt="border-medium-icon-right"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionRight="right"
          btnTxt="border-medium-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="medium"
          iconPositionCenter="center"
          btnTxt="border-medium-icon-center"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="medium"
          iconPositionCenter="center"
          btnTxt="border-medium-icon-center"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionCenter="center"
          btnTxt="border-medium-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="medium"
          iconPositionLeft="left"
          btnTxt="border-medium-icon-left"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="medium"
          iconPositionLeft="left"
          btnTxt="border-medium-icon-left"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionLeft="left"
          btnTxt="border-medium-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp hvBtn="base" btnSize="medium" btnTxt="hover-medium" />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="medium"
          btnTxt="hover-medium"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="medium"
          iconPositionRight="right"
          btnTxt="hover-medium-icon-right"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionRight="right"
          btnTxt="hover-medium-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="medium"
          iconPositionCenter="center"
          btnTxt="hover-medium-icon-center"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionCenter="center"
          btnTxt="hover-medium-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="medium"
          iconPositionLeft="left"
          btnTxt="hover-medium-icon-left"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="medium"
          iconPositionLeft="left"
          btnTxt="hover-medium-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp bgBtn="base" btnSize="small" btnTxt="default-small" />
        <ButtonCmp bgBtn="dark" btnSize="small" btnTxt="default-small" />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="small"
          btnTxt="default-small"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="default-small-icon-right"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="default-small-icon-right"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="small"
          iconPositionRight="right"
          btnTxt="default-small-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="default-small-icon-center"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="default-small-icon-center"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="default-small-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="default-small-icon-center"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="default-small-icon-center"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="default-small-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp bdBtn="base" btnSize="small" btnTxt="border-small" />
        <ButtonCmp bdBtn="dark" btnSize="small" btnTxt="border-small" />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="small"
          btnTxt="border-small"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="border-small-icon-right"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="border-small-icon-right"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="small"
          iconPositionRight="right"
          btnTxt="border-small-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="border-small-icon-center"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="border-small-icon-center"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="border-small-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="border-small-icon-left"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="border-small-icon-left"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="border-small-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp hvBtn="base" btnSize="small" btnTxt="hover-small" />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="small"
          btnTxt="hover-small"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="hover-small-icon-right"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="small"
          iconPositionRight="right"
          btnTxt="hover-small-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="small"
          icon
          btnTxt="hover-small-icon-center"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="small"
          icon
          btnTxt="hover-small-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          hvBtn="base"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="hover-small-icon-left"
        />
        <ButtonCmp
          hvBtn="disabled"
          disabled
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="hover-small-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp
          plusBtn="base"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="Add checkbox"
        />
      </div>
    </div>
    <title-input title="link" />
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="large"
          btnTxt="underline-large"
          :btnType="false"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="large"
          btnTxt="underline-large"
          :btnType="false"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="large"
          btnTxt="underline-large"
          :btnType="false"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bgBtn="base"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="underline-large-icon-right"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="dark"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="underline-large-icon-right"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="disabled"
          disabled
          btnSize="large"
          iconPositionRight="right"
          btnTxt="underline-large-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bgBtn="base"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="underline-large-icon-center"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="dark"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="underline-large-icon-center"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="disabled"
          disabled
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="underline-large-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bgBtn="base"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="underline-large-icon-left"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="dark"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="underline-large-icon-left"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="disabled"
          disabled
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="underline-large-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="large"
          btnTxt="default-large"
          :btnType="false"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="large"
          btnTxt="default-large"
          :btnType="false"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="large"
          btnTxt="default-large"
          :btnType="false"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bdBtn="base"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="default-large-icon-right"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="dark"
          btnSize="large"
          iconPositionRight="right"
          btnTxt="default-large-icon-right"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="disabled"
          disabled
          btnSize="large"
          iconPositionRight="right"
          btnTxt="default-large-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bdBtn="base"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="default-large-icon-center"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="dark"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="default-large-icon-center"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="disabled"
          disabled
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="default-large-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bdBtn="base"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="default-large-icon-left"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="dark"
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="default-large-icon-left"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="disabled"
          disabled
          btnSize="large"
          iconPositionLeft="left"
          btnTxt="default-large-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp
          bgBtn="base"
          btnSize="small"
          btnTxt="underline-small"
          :btnType="false"
        />
        <ButtonCmp
          bgBtn="dark"
          btnSize="small"
          btnTxt="underline-small"
          :btnType="false"
        />
        <ButtonCmp
          bgBtn="disabled"
          disabled
          btnSize="small"
          btnTxt="underline-small"
          :btnType="false"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bgBtn="base"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="underline-small-icon-right"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="dark"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="underline-small-icon-right"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="disabled"
          disabled
          btnSize="small"
          iconPositionRight="right"
          btnTxt="underline-small-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bgBtn="base"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="underline-small-icon-center"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="dark"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="underline-small-icon-center"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="disabled"
          disabled
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="underline-small-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bgBtn="base"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="underline-small-icon-left"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="dark"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="underline-small-icon-left"
        />
        <ButtonCmp
          :btnType="false"
          bgBtn="disabled"
          disabled
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="underline-small-icon-left"
        />
      </div>
    </div>
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp
          bdBtn="base"
          btnSize="small"
          btnTxt="default-small"
          :btnType="false"
        />
        <ButtonCmp
          bdBtn="dark"
          btnSize="small"
          btnTxt="default-small"
          :btnType="false"
        />
        <ButtonCmp
          bdBtn="disabled"
          disabled
          btnSize="small"
          btnTxt="default-small"
          :btnType="false"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bdBtn="base"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="default-small-icon-right"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="dark"
          btnSize="small"
          iconPositionRight="right"
          btnTxt="default-small-icon-right"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="disabled"
          disabled
          btnSize="small"
          iconPositionRight="right"
          btnTxt="default-small-icon-right"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bdBtn="base"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="default-small-icon-center"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="dark"
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="default-small-icon-center"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="disabled"
          disabled
          btnSize="small"
          iconPositionCenter="center"
          btnTxt="default-small-icon-center"
        />
      </div>
      <div class="guide-box">
        <ButtonCmp
          :btnType="false"
          bdBtn="base"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="default-small-icon-left"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="dark"
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="default-small-icon-left"
        />
        <ButtonCmp
          :btnType="false"
          bdBtn="disabled"
          disabled
          btnSize="small"
          iconPositionLeft="left"
          btnTxt="default-small-icon-left"
        />
      </div>
    </div>
    <title-input title="Social Button/Google" />
    <div class="guide__wrap">
      <div class="guide-box">
        <ButtonCmp
          bdBtn="google"
          btnSize="large"
          iconPositionCenter="center"
          btnTxt="Login with Google"
          @click="onClickGoogle()"
        />
      </div>
    </div>
    <title-input title="Icon Button" />
    <div class="guide__wrap">
      <div class="guide-box icon-box">
        <ButtonCmp
          bgBtn="icon-base"
          btnTxtHidden="노트 추가하기"
          @click="addNoteMove()"
        />
        <ButtonCmp
          bgBtn="icon-white"
          btnTxtHidden="노트 추가하기"
          @click="$router.push('/home')"
        />
        <ButtonCmp bgBtn="icon-dark" btnTxtHidden="노트 추가하기" />
        <ButtonCmp bgBtn="icon-light" btnTxtHidden="노트 추가하기" />
        <ButtonCmp
          bgBtn="icon-disabled"
          disabled
          btnTxtHidden="노트 추가하기"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import { useRouter } from 'vue-router'

const onClickGoogle = () => {
  // 구글 새 창 열기 (window.open 사용)
  window.open('http://google.com', '_blank')
}
// 메소드로 router 불러오기
const router = useRouter()
const addNoteMove = () => {
  router.push({
    path: '/home'
  })
}
</script>
