## Star-Rating-iOS-App


This is a 5 star rating app for iOS that offers a simple interface and implementation with float return and setup. 

How to use: 
Add RatingCustomView to your project. 
You'd also need the starRatingMask.png from Assets.xcassets
Then in your view controller do:

    override func viewDidLoad()
    {
        super.viewDidLoad()
        
        self.view.layoutIfNeeded();
        self.view.layoutSubviews();
        
        let ratingContentView = RatingCustomView (frame: ratingContainer.bounds);
        ratingContainer.addSubview(ratingContentView );
        ratingContentView.delegate = self;
    }
    
    // ratingContainer is the view where the rating should stick to.
    // the delegation is only there to show you the actual label change.
    // the actual rate value can be read from:
    ratingContentView.rate
    
    The rating is truncated into a single decimal point (i.e. 1.1). You can change that in RatingCustomView in function called rateAt. Change the 50 to 500 and 10 to 100 to get 2 decimal points and so on and so forth. 


![alt text](https://github.com/AmirJahan/Swift_Star-Rating/blob/master/Swift_Star-Rating.gif?raw=true)
