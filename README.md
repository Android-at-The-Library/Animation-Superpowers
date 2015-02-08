# Animation-Superpowers
Adding basic animations to Images and Buttons of your app.


## ViewPropertyAnimator


## Absolute Destination

This animation will move the object to the specified coordinate.

Change the three nubers in the `bob.animate...` line to adjust the final x and y coordinates, 
as well as the animation's duration (in milliseconds, so `1000` will be one second).

1. Just above the `@Override` of the `onCreate` method, add `private ImageView imageView;`

It should look like this:

```java
    private ImageView imageView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
```

2. add this beneath your `setContentsView(...)` section line

```java
imageView = (ImageView) findViewById(R.id.imageView);

public Button bob = (Button) findViewById(R.id.button);

bob.setOnClickListener( new View.onClickListener() {
  public void onClick(View v) {
    bob.animate().x(100).y(100).setDuration(500);
  }
});
```

## Relative Movement

This animation will simply offset the object by a given amount.

1. Just above the `@Override` of the `onCreate` method, add `private ImageView imageView;`

It should look like this:

```java
    private ImageView imageView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
```

2. add this beneath your `setContentsView(...)` section line

```java
imageView = (ImageView) findViewById(R.id.imageView);

public Button bob = (Button) findViewById(R.id.button);

bob.setOnClickListener( new View.onClickListener() {
  public void onClick(View v) {
    bob.animate().translationXBy(100).translationYBy(100).setDuration(500);
  }
});
```
