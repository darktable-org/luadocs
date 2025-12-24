---
title: overview
id: overview
weight: 10
draft: false
author: "people"
---

darktable can be customized and extended using the Lua programming language. The [lua-scripts repository](https://github.com/darktable-org/lua-scripts)
contains the collected
efforts of the darktable developers, maintainers, contributors and community. The following sections list the scripts
contained in the repository, whether they can be run by themselves (Standalone - Yes) or depend on other
scripts (Standalone - No), what operating systems they are known to work on (L - Linux, M - MacOS, W - Windows), and their purpose.

### Official Scripts

These scripts are written primarily by the darktable developers and maintained by the authors and/or repository maintainers. They are located in the official/ directory.

Name|Standalone|Op/Sys |Purpose
----|:--------:|:-----:|-------
[apply_camera_style](official/apply_camera_style.md)|Yes|LMW|Apply camera styles to images
[check_for_updates](official/check_for_updates.md)|Yes|LMW|Check for updates to darktable
[copy_paste_metadata](official/copy_paste_metadata.md)|Yes|LMW|Copy and paste metadata, tags, ratings, and color labels between images
[delete_long_tags](official/delete_long_tags.md)|Yes|LMW|Delete all tags longer than a specified length
[delete_unused_tags](official/delete_unused_tags.md)|Yes|LMW|Delete tags that have no associated images
[enfuse](official/enfuse.md)|No|L|Exposure blend several images (HDR)
[generate_image_txt](official/generate_image_txt.md)|No|L|Generate txt sidecar files to be overlaid on zoomed images
[image_path_in_ui](official/image_path_in_ui.md)|Yes|LMW|Plugin to display selected image path
[import_filter_manager](official/import_filter_manager.md)|Yes|LMW|Manager for import filters
[import_filters](official/import_filters.md)|No|LMW|Two import filters for use with import_filter_manager
[regenerate_thumbnails](official/regenerate_thumbnails.md)|Yes|LMW|Regenerate missing lighttable thumbnails
[save_selection](official/save_selection.md)|Yes|LMW|Provide save and restore from multiple selection buffers
[selection_to_pdf](official/selection_to_pdf.md)|No|L|Generate a PDF file from the selected images


### Contributed Scripts

These scripts are contributed by users. They are meant to have an "owner", i.e. the author, who maintains them. Over time the community has helped maintain these scripts, as well as the authors. They are located in the contrib/ directory.

Name|Standalone|Op/Sys |Purpose
----|:--------:|:-----:|-------
[AutoGrouper](contrib/AutoGrouper.md)|Yes|LMW|Group images together by time
[autostyle](contrib/autostyle.md)|Yes|LMW|Automatically apply styles on import
[clear_GPS](contrib/clear_GPS.md)|Yes|LMW|Reset GPS information for selected images
[CollectHelper](contrib/CollectHelper.md)|Yes|LMW|Add buttons to selected images module to manipulate the collection
[copy_attach_detach_tags](contrib/copy_attach_detach_tags.md)|Yes|LMW|Copy and paste tags from/to images
[cr2hdr](contrib/cr2hdr.md)|Yes|L|Process image created with Magic Lantern Dual ISO
[enfuseAdvanced](contrib/enfuseAdvanced.md)|No|LMW|Merge multiple images into Dynamic Range Increase (DRI) or Depth From Focus (DFF) images
[exportLUT](contrib/exportLUT.md)|Yes|LMW|Create a LUT from a style and export it
[ext_editor](contrib/ext_editor.md)|No|LW|Export pictures to collection and edit them with up to nine user-defined external editors
[face_recognition](contrib/face_recognition.md)|No|LM|Identify and tag images using facial recognition
[fujifilm_ratings](contrib/fujifilm_ratings.md)|No|LM|Support importing Fujifilm ratings
[geoJSON_export](contrib/geoJSON_export.md)|No|L|Create a geo JSON script with thumbnails for use in ...
[geoToolbox](contrib/geoToolbox.md)|No|LMW|A toolbox of geo functions
[gimp](contrib/gimp.md)|No|LMW|Open an image in GIMP for editing and return the result
[gpx_export](contrib/gpx_export.md)|No|LMW|Export a GPX track file from selected images GPS data
[HDRMerge](contrib/HDRMerge.md)|No|LMW|Combine the selected images into an HDR DNG and return the result
[hugin](contrib/hugin.md)|No|LMW|Combine selected images into a panorama and return the result
[image_stack](contrib/image_stack.md)|No|LMW|Combine a stack of images to remove noise or transient objects
[image_time](contrib/image_time.md)|Yes|LMW|Adjust the EXIF image time
[kml_export](contrib/kml_export.md)|No|L|Export photos with a KML file for usage in Google Earth
[LabelsToTags](contrib/LabelsToTags.md)|Yes|LMW|Apply tags based on color labels and ratings
[OpenInExplorer](contrib/OpenInExplorer.md)|No|LMW|Open the selected images in the system file manager
[passport_guide](contrib/passport_guide.md)|Yes|LMW|Add passport cropping guide to darkroom crop tool
[pdf_slideshow](contrib/pdf_slideshow.md)|No|LM|Export images to a PDF slideshow
[photils](contrib/photils.md)|No|LM|Automatic tag suggestions for your images
[quicktag](contrib/quicktag).md|Yes|LMW|Create shortcuts for quickly applying tags
[rate_group](contrib/rate_group.md)|Yes|LMW|Apply or remove a star rating from grouped images
[rename-tags](contrib/rename-tags.md)|Yes|LMW|Change a tag name
[RL_out_sharp](contrib/RL_out_sharp.md)|No|LW|Output sharpening using GMic (Richardson-Lucy algorithm)
[select_untagged](contrib/select_untagged.md)|Yes|LMW|Enable selection of untagged images
[slideshowMusic](contrib/slideshowMusic.md)|No|L|Play music during a slideshow
[transfer_hierarchy](contrib/transfer_hierarchy.md)|Yes|LMW|Image move/copy preserving directory hierarchy
[video_ffmpeg](contrib/video_ffmpeg.md)|No|LMW|Export video from darktable

### Example Scripts

These scripts provide examples of how to use specific portions of the API. They run, but are meant for demonstration purposes only. They are located in the examples/ directory.

Name|Standalone|Op/Sys |Purpose
----|:--------:|:-----:|-------
[api_version](examples/api_version.md)|Yes|LMW|Print the current API version
[darkroom_demo](examples/darkroom_demo.md)|Yes|LMW|Demonstrate changing images in darkoom 
[gettextExample](examples/gettextExample.md)|Yes|LM|How to use translation
[hello_world](examples/hello_world.md)|Yes|LMW|Prints hello world when darktable starts
[lighttable_demo](examples/lighttable_demo.md)|Yes|LMW|Demonstrate controlling lighttable mode, zoom, sorting and filtering
[moduleExample](examples/moduleExample.md)|Yes|LMW|How to create a lighttable module
[multi_os](examples/multi_os.md)|No|LMW|How to create a cross platform script that calls an external executable
[panels_demo](examples/panels_demo.md)|Yes|LMW|Demonstrate hiding and showing darktable panels
[preferenceExamples](examples/preferenceExamples.md)|Yes|LMW|How to use preferences in a script
[printExamples](examples/printExamples.md)|Yes|LMW|How to use various print functions from a script
[running_os](examples/running_os.md)|Yes|LMW|Print out the running operating system

### Tools

Tool scripts perform functions relating to the repository, such as generating documentation. They are located in the tools/ directory.

Name|Standalone|Op/Sys |Purpose
----|:--------:|:-----:|-------
[executable_manager](tools/executable_manager.md)|Yes|LMW|Manage the external executables used by the lua scripts
[gen_i18n_mo](tools/gen_i18n_mo.md)|No|LMW|Generate compiled translation files (.mo) from source files (.po)
[get_lib_manpages](tools/get_lib_manpages.md)|No|LM|Retrieve the library documentation and output it in man page and PDF format
[get_libdoc](tools/get_libdoc.md)|No|LMW|Retrieve the library documentation and output it as text
[script_manager](tools/script_manager.md)|No|LMW|Manage (install, update, enable, disable) the lua scripts
