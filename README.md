# ExpandableTextView

This project provides a sample SwiftUI based integration for the [TextExpander SDK][TextExpander].

The SDK integration is provided by the custom [`ExpandableTextView`][ExpandableTextView] SwiftUI view. This provides a simple, reusable, (almost) self-contained component to quickly support the TextExpander SDK in any SwiftUI based app. This supports the following TextExpander features:

* inline snippets expansion
* fill-in support for complex snippets (done externally by the TextExpander app)
* simple snippets library management (e.g., synchronization, clearing, etc)

The [`ExpandableTextView`][ExpandableTextView] view wraps a `UITextView`, providing all expected multi-line text editing capabilities. The `UITextView` delegate is implemented by an internal, per view `SMTEDelegateController` instance. The global TextExpander settings are controlled by the [`TextExpanderStatus`][TextExpanderStatus] singleton.

Finally, the sample app shows two `ExpandableTextEditor` working side by side plus some global settings, as demonstrated by the video below:

https://user-images.githubusercontent.com/3756628/117472602-7408f580-af2f-11eb-90fb-75faf4737b45.mp4

## Future Ideas

In the future, we could extend this in the following ways:

* Support for [rich text editing][Rich Text] (i.e., attributed strings, etc).
* Expose this as a proper Swift Package framework around the aforementioned reusable `ExpandableTextView`.
* Improve the `ExpandableTextView` API, providing per view settings such as: turning off snippets expansion; turning off fill-in support; etc.
* Provide more information about the number of available snippets, last synchronization date, etc.

[TextExpander]: https://github.com/SmileSoftware/TextExpanderTouchSDK/blob/master/README.md
[ExpandableTextView]: https://github.com/pmattos/ExpandableTextEditor/blob/main/ExpandableTextView/ExpandableTextView.swift
[TextExpanderStatus]: https://github.com/pmattos/ExpandableTextEditor/blob/main/ExpandableTextView/TextExpanderStatus.swift
[Rich Text]: https://github.com/SmileSoftware/TextExpanderTouchSDK/blob/master/README.md#handling-attributed-text

