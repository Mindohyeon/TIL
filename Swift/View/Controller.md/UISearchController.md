# UISearchController
iOS 에서 SearchBar 를 구현하는 방법은 2가지가 있다.
- UISearchBar
- UISearchController

## UISearchController 란?
검색창과 상호작용하는 것을 베이스로 검색 결과를 보여주는 것을 관리하는 컨트롤러이다.

UISearchBar 와 함께 사용자와 상호작용할 때 UISearchController 는 검색 결과 컨트롤러를 통해 검색 결과를 표시한다.

UISearchController 안에 SearchBar 가 포함되어 있다.

#### init(searchResultsController: UIViewController?)
UISearchController 클래스의 initialize 이다.

searchResult 를 두 번쨰 뷰 컨트롤러를 통해 검색 결과를 보여주려고 할 때 init(searchResultsController:)에 해주면 된다.
이렇게 해주면 사용자가 searchBar 와 함께 상호작용할 때 searchController 는 자동적으로 결과 컨트롤러를 통해 결괏값 보여준다.

