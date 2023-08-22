# carbonkit-spm

This is a version of the CarbonKit library that has been adapted to be compatible with Swift Package Manager (SPM). The original CarbonKit repository can be found at: [https://github.com/ermalkaleci/CarbonKit](https://github.com/ermalkaleci/CarbonKit)

## About CarbonKit

CarbonKit is an open source iOS library that provides powerful and visually appealing UI components for your projects. It includes the following components:

- CarbonSwipeRefresh
- CarbonTabSwipeNavigation

## Installation

You can integrate CarbonKit into your project using Swift Package Manager.

### Swift Package Manager

1. Open your Xcode project.
2. Select your project in the Project Navigator.
3. Navigate to the Swift Packages tab.
4. Click the "+" button to add a package.
5. Enter the URL of this repository: `https://github.com/leventozgur/carbonkit-spm`
6. Choose the version rule according to your preferences.
7. Click Next, then Finish.

## Usage

After adding CarbonKit as a Swift Package, you can import and use its components in your code. Here's a simple example:

```swift
import CarbonKit_spm

class ViewController: UIViewController, CarbonTabSwipeNavigationDelegate {

    // MARK: Override methods
    override func viewDidLoad() {
        super.viewDidLoad()
        let items = ["Features", "Products", "About"]
        let carbonTabSwipeNavigation = CarbonTabSwipeNavigation(items: items, delegate: self)
        carbonTabSwipeNavigation.insertIntoRootViewController(self)
		// or carbonTabSwipeNavigation.insertIntoRootViewController(self, andTargetView: yourView)
    }

    func carbonTabSwipeNavigation(carbonTabSwipeNavigation: CarbonTabSwipeNavigation, viewControllerAtIndex index: UInt) -> UIViewController {
        // return viewController at index
    }
}
