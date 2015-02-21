# Animation-Superpowers

Adding basic animations to Images and Buttons of your app.



**Common Step 1) for all examples**

**NOTE** These examples require you to place an imageView declaration just above the `@Override` of the `onCreate` method, add `private Button bob;`

It should look like this just above the `onCreate`:

```java
    private Button bob;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
```


## ViewPropertyAnimator - Absolute Destination

This animation will move the object to the specified coordinate.

Change the three numbers in the `bob.animate...` line to adjust the final x and y coordinates, 
as well as the animation's duration (in milliseconds, so `1000` will be one second).

Step 2)

 add this beneath your `setContentsView(...)` section line

```java
bob = (Button) findViewById(R.id.button);

bob.setOnClickListener( new View.OnClickListener() {
  public void onClick(View v) {
    imageView.animate().x(100).y(100).setDuration(500);
  }
});
```

## ViewPropertyAnimator - Relative Movement

This animation will simply offset the object by a given amount.


Step 2) 

add this beneath your `setContentsView(...)` line:

```java
bob = (Button) findViewById(R.id.button);

bob.setOnClickListener( new View.OnClickListener() {
  public void onClick(View v) {
    imageView.animate().translationXBy(100).translationYBy(100).setDuration(500);
  }
});
```


## ViewPropertyAnimator - Scale Animation (Absolute)


scaleY (and scaleX) will scale the view by a floating point value.

For example, use the number `2.0f` to do an animation for scaling to 200% of the initial height.

Step 2)

add this beneath your `setContentsView(...)` line:

```java
bob = (Button) findViewById(R.id.button);

bob.setOnClickListener( new View.OnClickListener() {
  public void onClick(View v) {
    bob.animate().scaleY(1.5f).setDuration(500);
  }
});
```

## ViewPropertyAnimator - Scale Animation (Relative)

scaleYBy (and scaleXBy) will scale the view by a given amount.

add this beneath your `setContentsView(...)` line

```java
bob = (Button) findViewById(R.id.button);

bob.setOnClickListener( new View.OnClickListener() {
    public void onClick(View v) {
    bob.animate().scaleYBy(1.5f).setDuration(500);
    }
});
```
