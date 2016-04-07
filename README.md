#TBEmptyDataSet
TBEmptyDataSet is an extension of UITableView/UICollectionView's super class, it will  display a placeholder emptyDataSet when the data of tableView/collectionView is empty.

TBEmptyDataSet can be composed of an image, a title and a description, or you can set it as a custom view.


![Example](Screenshots/Example.gif "Example")


##How To Get Started
###Carthage
Specify "TBEmptyDataSet" in your ```Cartfile```:
```ogdl 
github "teambition/TBEmptyDataSet"
```

###CocoaPods
Specify "TBEmptyDataSet" in your ```Podfile```:
```ruby 
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'
use_frameworks!

pod 'TBEmptyDataSet'
```

###Usage
##### 1.  Assign the data source and delegate
```swift
tableView.emptyDataSetDataSource = self
tableView.emptyDataSetDelegate = self
```
##### 2.  Implement the data source and delegate
Data source functions:
```swift 
func imageForEmptyDataSet(scrollView: UIScrollView!) -> UIImage? {
    // return the image for EmptyDataSet
}

func titleForEmptyDataSet(scrollView: UIScrollView!) -> NSAttributedString? {
    // return the title for EmptyDataSet
}

func descriptionForEmptyDataSet(scrollView: UIScrollView!) -> NSAttributedString? {
    // return the description for EmptyDataSet
}

func imageTintColorForEmptyDataSet(scrollView: UIScrollView!) -> UIColor? {
    // return the image tint color for EmptyDataSet
}

func backgroundColorForEmptyDataSet(scrollView: UIScrollView!) -> UIColor? {
    // return the backgroundColor for EmptyDataSet
}

func verticalOffsetForEmptyDataSet(scrollView: UIScrollView!) -> CGFloat {
    // return the vertical offset for EmptyDataSet, default is 0
}

func verticalSpacesForEmptyDataSet(scrollView: UIScrollView!) -> [CGFloat] {
    // return the vertical spaces from top to bottom for EmptyDataSet, default is [12, 12]
}

func customViewForEmptyDataSet(scrollView: UIScrollView!) -> UIView? {
    // return an UIView instance for EmptyDataSet
}
``` 
Delegate functions:
```swift
func emptyDataSetShouldDisplay(scrollView: UIScrollView!) -> Bool {
    // should display EmptyDataSet or not, default is true
}

func emptyDataSetTapEnabled(scrollView: UIScrollView!) -> Bool {
    // enable tap gesture or not, default is true
}

func emptyDataSetScrollEnabled(scrollView: UIScrollView!) -> Bool {
    // scrollView can scroll or not, default is false
}

func emptyDataSetDidTapView(scrollView: UIScrollView!) {
    // do something
}

func emptyDataSetWillAppear(scrollView: UIScrollView!) {
    // do something
}

func emptyDataSetDidAppear(scrollView: UIScrollView!) {
    // do something
}

func emptyDataSetWillDisappear(scrollView: UIScrollView!) {
    // do something
}

func emptyDataSetDidDisappear(scrollView: UIScrollView!) {
    // do something
}
```

## Minimum Requirement
iOS 8.0

## Release Notes
* [Release Notes](https://github.com/teambition/TBEmptyDataSet/releases)

## License
TBEmptyDataSet is released under the MIT license. See [LICENSE](https://github.com/teambition/TBEmptyDataSet/blob/master/LICENSE.md) for details.

## More Info
Have a question? Please [open an issue](https://github.com/teambition/TBEmptyDataSet/issues/new)!