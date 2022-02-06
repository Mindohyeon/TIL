# UISearchBar
사용자로부터 검색 연관된 정보를 받기 위한 특별한 뷰이다.
UISearchBar 는 <b>entering text, 검색 버튼, 북마크 버튼, 취소 버튼을 제공한다.</b>

UISearchBar 는 쌩 날것으로 그냥 구현하면 검색기능을 수행하지 않는다. 즉, <b>UISearchBarDelegate 프로토콜</b>을 사용하여 유저가 텍스트를 쓰고 엔터를 치거나 버튼을 클릭했을 때 동작을 구현하게 해준다.

다른 특징으로는 appearance 프록시를 사용해서 앱에 있는 모든 searchBar 의 외형을 일괄적으로 커스텀할 수 있다.