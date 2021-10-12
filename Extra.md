# Intent putExtra 란?

android 에서 액티비티간에 이동을 위해 Intent 를 사용한다.

만약 액티비티 이동과 동시에 이전 액티비티에서 이동하는 액티비티로 값을 넘기고 싶다면 <b>Intent 안에 있는 putExtra 함수를 호출하면 된다.</b>

## putExtra
키 값과 value 값으로 이동하는 액티비티로 전달되며 다양한 value 값을 넘겨줄 수 있다.

## getExtra
getExtra 를 사용해서 값을 받을 수 있다.

<b>putExtra으로 보내고 getExtra로 받는다.</b>