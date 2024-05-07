#include <iostream>
#include <vector>

using namespace std;

// Function to perform Binary Search
int binarySearch(const vector<int>& arr, int target) {
    int left = 0; // Left boundary of the search interval
    int right = arr.size() - 1; // Right boundary of the search interval

    while (left <= right) {
        int mid = left + (right - left) / 2; // Calculate the mid point

        // Check if the target is present at mid
        if (arr[mid] == target) {
            return mid;
        }

        // If target is greater, ignore left half
        if (arr[mid] < target) {
            left = mid + 1;
        }
        // If target is smaller, ignore right half
        else {
            right = mid - 1;
        }
    }

    // If the target is not found
    return -1;
}

// Function to print the result of Binary Search
void printResult(int result, int target) {
    if (result != -1) {
        cout << "Element " << target << " is present at index " << result << endl;
    } else {
        cout << "Element " << target << " is not present in the array" << endl;
    }
}

int main() {
    vector<int> arr = {2, 3, 4, 10, 40};
    int target = 10;

    int result = binarySearch(arr, target);
    printResult(result, target);

    target = 5;
    result = binarySearch(arr, target);
    printResult(result, target);

    return 0;
}
